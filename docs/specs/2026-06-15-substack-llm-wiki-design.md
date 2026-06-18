# Design: LLM-Wiki memory for the Substack Scanner

**Date:** 2026-06-15
**Status:** Approved — implementing
**Routine:** Substack Scanner (`trig_016JHS66WHLATunNQ1xVRXhP`)
**Repo:** `YilinShao-WeighedSalt/Substack-analysis` (public)

## Goal

Give the Substack Scanner a **persistent, compounding memory** so each report is written with knowledge of everything seen before, instead of cold-reading the last 3 days every run. The agent should be able to say things like *"this is the 4th bullish LITE call since April; the prior three are up ~12% — thesis is tracking,"* or *"Citrini's last three 'overvalued' calls were early/wrong, discount accordingly."*

The memory follows the **`nashsu/llm_wiki` pattern**: an incrementally-maintained, interlinked markdown wiki committed to the repo — explicitly *not* RAG (no re-deriving from scratch, no vector server). The same vault is browsable locally in the `llm_wiki` desktop app (graph view, search, lint).

## Non-goals

- Not changing the emailed deliverable. The HTML report and ntfy push/email stay exactly as they are; the wiki *informs* the report, it does not replace it.
- Not running any external engine in the cloud sandbox. The wiki is plain files; the agent maintains them with Read/Write/Bash + existing MCPs.
- Not a human-in-the-loop ingest. The routine is unattended (see Deviations).

## Constraints

1. **Fresh sandbox every run.** The routine starts from a clean `git clone` with zero memory. The only persistence is what gets committed to the repo. → The wiki lives in the repo, read at run start, updated at run end, committed.
2. **`llm_wiki` desktop app is local-only.** Its MCP server bridges to `http://127.0.0.1:19828` on the user's machine; the cloud sandbox cannot reach it. → The cloud routine only ever touches files; the app is the user's local lens on those same files.
3. **Context budget.** The wiki grows forever. The agent must never read the whole thing — only entries relevant to the current run (index-routed reads).
4. **App schema compatibility.** For the user to open the vault in `llm_wiki`, files must conform to its schema contract.

## `llm_wiki` compatibility contract (extracted from the app source)

- **`schema.md`** at repo root with a `## Page Types` section: a markdown table `| type | wiki/<dir>/ | purpose |`. The app's parser routes/validates pages by this table (type matches `^[a-z][a-z0-9_-]*$`; dir is `wiki` or `wiki/...`). Types are user-defined.
- **Frontmatter** (YAML, every page): `type`, `title`, `tags`, `related`, `created`, `updated`. `source` pages also: `authors`, `year`, `url`, `venue`. Parser is lenient (recovers stray ```yaml fences and unbracketed `[[wikilink]]` lists).
- **`index.md`** — catalog grouped by type; entries `- [[page-slug]] — one-line description`.
- **`log.md`** — reverse-chronological; `## YYYY-MM-DD` headers, `- action` bullets.
- **Links:** `[[page-slug]]`. **Filenames:** `kebab-case.md`.

## Vault structure

```
schema.md                      # page-type routing table (app reads this)
wiki/
  index.md                     # catalog, grouped by type — agent reads FIRST
  log.md                       # append-only run log
  overview.md                  # type: overview — what this wiki is, current market read
  sources/   <pub>-YYYY-MM-DD-<slug>.md
  tickers/   <TICKER>.md
  publications/ <handle>.md
  themes/    <slug>.md
  synthesis/ <slug>.md
  queries/   <slug>.md
reports/YYYY-MM-DD.html         # existing deliverable, unchanged
```

### Page types (the `schema.md` table)

| type | dir | purpose |
|------|-----|---------|
| source | wiki/sources/ | One ingested post: full summary, extracted calls, link to original |
| ticker | wiki/tickers/ | Running dossier: call log, thesis evolution, outcome tracking |
| publication | wiki/publications/ | Per-publication track record, style, hit-rate |
| theme | wiki/themes/ | Narrative/thesis timelines across posts and publications |
| synthesis | wiki/synthesis/ | Cross-cutting conclusions (consensus vs. contrarian, sector reads) |
| query | wiki/queries/ | Open questions / contradictions being tracked |
| overview | wiki/ | One-page project overview + current high-level market read |

### Ticker dossier body (the heart)

```
## Call log
| date | publication | stance | px@call | thesis (1 line) |
|------|-------------|--------|---------|-----------------|
| 2026-04-12 | [[irrationalanalysis]] | LONG | 78 | laser-linewidth edge |
| 2026-06-07 | [[irrationalanalysis]] | LONG | 91 | datacenter ramp |

## Thesis evolution
<prose: how the narrative changed, who's bullish/bearish and why>

## Outcome tracking
<prose: px@call vs current; is the thesis playing out? what would falsify it?>
```

## Outcome tracking mechanic

Each call row stores **`px@call`** — the price at call time. For ongoing runs, fetched via the yfinance MCP when a call is logged; later runs fetch current price and compute the return since each prior call. For the bootstrap, `px@call` is taken from the price the report itself recorded for that ticker on that date (`n/a` where absent).

## Routine run flow (changes to the existing prompt)

Existing Steps 0–8 wrapped with wiki read/write:

1. **Step 0** (unchanged): 3-day fire-day gate.
2. **Step 1a — Load memory (NEW):** read `wiki/index.md` + `wiki/log.md`; load only the ticker/publication/theme/source pages relevant to the current scan. Never read the whole vault.
3. **Steps 1–5** (existing scan/summarize/analyze/ticker-deep-dive): now memory-aware — reference prior calls, outcomes, track records, theme history.
4. **Step 6 — Write HTML report** (existing): now includes "vs. prior calls / outcome" context.
5. **Step 6a — Ingest (NEW):** per new post create a `source` page; update affected `ticker` pages (append call rows with `px@call`, refresh outcomes), `publication` pages, `theme` pages; update `index.md`; append `log.md`. A run may touch 10–20 pages.
6. **Step 7 — Commit & push** (widened): stage `reports/` **and** `wiki/` + `schema.md`; one commit; push.
7. **Step 8 — ntfy** (unchanged): push + email with the rendered report link.

## Bootstrap (one-time seeding)

Seed the wiki from the **6 existing reports** (2026-06-01 → 2026-06-16). A one-time cloud routine reads each report, extracts posts → `source` pages, tickers → `ticker` dossiers with back-dated call rows, recurring themes → `theme` pages, per-publication tallies → `publication` pages; writes `schema.md`, `index.md`, `log.md`, `overview.md`; commits and pushes. `px@call` from the report's recorded price, else `n/a`.

## Using the `llm_wiki` app (local)

The user points the desktop app at the cloned repo as a project. The app reads `schema.md` + the vault and provides graph view, search, lint. **Validation step:** after the first vault exists, open it once in the app to confirm the schema table and frontmatter parse cleanly (the one residual compatibility unknown).

## Scaling strategy

- **Index-routed reads:** read `index.md` first, pull only relevant pages. Per-run cost stays roughly flat.
- **Per-entity files:** one ticker/theme/publication per file → only ~8 active entities per run touched.
- **Periodic lint (light):** ~monthly, an `llm_wiki`-style lint pass (contradictions, stale theses, orphans, missing cross-refs).

## Deviations from `llm_wiki` (intentional)

`llm_wiki` assumes interactive human-in-the-loop ingest. Ours is **unattended** — the routine ingests autonomously every 3 days. Compatible with the file format; human involvement moves to *after the fact* (browse/query/lint in the app).

## Risks & open questions

- **App opens an externally-authored vault:** very likely (contract from source), confirmed by the validation step.
- **Context growth over months:** mitigated by index-routed reads; revisit with a CLI search tool (`qmd`) if needed.
- **Run length / cost:** ingest adds writes per run; acceptable at 3-day cadence; watch first runs.
- **`px@call` for back-dated calls:** some unavailable → `n/a`, not fatal.

## Success criteria

1. A new report visibly references prior calls/outcomes and track records that exist only in the wiki.
2. The vault opens cleanly in the `llm_wiki` desktop app with a populated graph.
3. A full unattended run completes and the report email still arrives.
4. The wiki grows across runs without per-run context load growing materially.

## Out of scope (for now)

- A CLI search engine (`qmd`) — only if the index stops sufficing.
- Applying the wiki to the other two routines.
- Any change to ntfy, environment, or schedule.

## Implementation phases

1. **Schema & skeleton:** `schema.md` + `wiki/` dirs + `index.md`/`log.md`/`overview.md`.
2. **Bootstrap:** one-time cloud run seeds from the 6 reports; commit + push.
3. **Validate in app:** user opens the vault locally; fix any mismatch.
4. **Rewrite routine prompt:** add Steps 1a + 6a, widen Step 7; update via RemoteTrigger.
5. **Verify end-to-end:** manual run; confirm report references memory and email arrives.
