# Wiki Schema — Substack Investment Scan

This `wiki/` is the persistent memory of the **Substack Scanner** routine. It is
maintained automatically by an unattended agent every 3 days, and is browsable
locally in the `llm_wiki` desktop app (point it at this repo). It follows the
`nashsu/llm_wiki` pattern: an incrementally-built, interlinked markdown wiki —
not RAG. Prefer appending over rewriting; do not destroy history.

## Page Types

| type | directory | purpose |
|------|-----------|---------|
| source | wiki/sources/ | One ingested Substack post: full summary, extracted calls, link to original |
| ticker | wiki/tickers/ | Per-ticker dossier: call log, thesis evolution, outcome tracking |
| publication | wiki/publications/ | Per-publication track record, style, and hit-rate |
| theme | wiki/themes/ | Narrative / thesis timelines across posts and publications |
| synthesis | wiki/synthesis/ | Cross-cutting conclusions (consensus vs. contrarian, sector reads) |
| query | wiki/queries/ | Open questions and unresolved contradictions being tracked |
| overview | wiki/ | One-page overview of the wiki and current high-level market read (one per project) |

## Naming Conventions

- Files: `kebab-case.md`
- Tickers: uppercase symbol — `LITE.md`, `MU.md`
- Publications: substack handle — `semianalysis.md`, `irrationalanalysis.md`
- Sources: `<handle>-YYYY-MM-DD-<slug>.md` — `semianalysis-2026-06-13-hbm4-supply.md`
- Themes: descriptive noun phrase — `hbm4-supply-tightness.md`, `token-panic.md`

## Frontmatter

All pages include:

```yaml
---
type: source | ticker | publication | theme | synthesis | query | overview
title: Human-readable title
tags: []
related: []
created: YYYY-MM-DD
updated: YYYY-MM-DD
---
```

Source pages also include:

```yaml
authors: [<handle>]
year: YYYY
url: ""
venue: <publication name>
post_date: YYYY-MM-DD
tickers: [LITE, MU]
```

Ticker pages also include:

```yaml
ticker: LITE
current_stance: long | short | neutral | mixed
conviction: high | medium | low
last_review: YYYY-MM-DD
```

Publication pages also include:

```yaml
handle: semianalysis
calls_logged: 0
hit_rate: "n/a"
```

Theme pages also include:

```yaml
status: emerging | maturing | consensus | fading
first_seen: YYYY-MM-DD
```

## Index Format

`wiki/index.md` lists every page grouped by type. Each entry:

```
- [[page-slug]] — one-line description
```

## Log Format

`wiki/log.md` records each run in reverse chronological order:

```
## YYYY-MM-DD
- ingest | <N> posts from <pubs> | tickers touched: <list>
```

## Cross-referencing Rules

- Link between pages with `[[page-slug]]`.
- Every source page links the tickers, publications, and themes it touches via `related:` and inline `[[...]]`.
- Ticker, publication, and theme pages link back to the source pages that mention them.
- When publications contradict each other on a ticker, note it on the ticker page and open/append a `query` page linking both sides.

## Ticker dossier body format

Each ticker page body contains, in order:

### Call log

A markdown table; append the newest row each run, never rewrite prior rows:

```
| date | publication | stance | px@call | thesis (1 line) |
|------|-------------|--------|---------|-----------------|
```

`stance` ∈ LONG / SHORT / NEUTRAL / HEDGE. `px@call` is the price at the time of
the call (number, or `n/a` if unknown).

### Thesis evolution

Prose: how the narrative changed over time; who is bullish/bearish and why.

### Outcome tracking

Prose: `px@call` vs. current price; is the thesis playing out; what would falsify it.

## Maintenance conventions (for the unattended agent)

- Read `wiki/index.md` FIRST; load only the pages relevant to the current scan. Never read the whole wiki.
- Touch only entities that appear in the current scan, plus their existing dossiers.
- Append to call logs; never rewrite history. Correct an error by adding a dated note, not by deleting.
- A single run may touch 10–20 pages. Update `index.md` and append one `log.md` entry every run.
- About monthly, do a lint pass: flag contradictions, stale theses, orphan pages, missing cross-references.
