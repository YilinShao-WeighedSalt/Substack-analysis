---
type: source
title: "Semi Doped — OpenAI's Jalapeño! Feeling Hot Hot Hot! (podcast)"
tags: [custom-silicon, inference, asic, educational]
related: ["[[semidoped]]", "[[custom-silicon-asic]]", "[[ai-accelerator-competition]]", "[[AVGO]]", "[[eda-chip-design]]"]
created: 2026-08-30
updated: 2026-08-30
authors: [semidoped]
year: 2026
url: "https://daily.semidoped.com/p/new-episode-openais-jalapeno-feeling"
venue: Semi Doped
post_date: 2026-08-27
tickers: []
---

# OpenAI's Jalapeño — Hot Chips teardown (podcast)

**Educational — no new priced calls** (Jalapeño's equity read was priced by SemiAnalysis on Aug-25 → [[AVGO]] LONG). Austin & Vik break down the architecture within 12 hours of the Hot Chips talk (OpenAI team: Richard Ho [ex-Google TPU], Ravi [chip architect], Chris [SW co-design]).

## Concept takeaways (feeds [[custom-silicon-asic]] / [[ai-accelerator-competition]])

- **Design goal = user experience, not TCO.** The two metrics: **end-to-end latency (time to *last* token)** and **energy per request** — explicitly at odds, so OpenAI reports **Pareto-frontier curves** rather than single numbers. Notable because a *model lab* designing chips optimizes for the end AI user, not the silicon *buyer* (unlike merchant vendors who sell on TCO).
- **NUMA-style local HBM slices** — memory partitioned into locality domains per compute tile.
- **Scale-up networking with Broadcom + ESUN** — open scale-up fabric (the NVLink alternative).
- **"Dark silicon is cheaper than idle accelerators"** — a balanced-design philosophy: over-provision some blocks rather than stall the expensive units.
- **~9-month RTL-to-tapeout** using AI-assisted EDA (Codex-written kernels) — the compressed design cycle is the competitive-landscape shock.

Reinforces the thread: AI can help labs build great chips fast — the open question is whether state/local governments will permit and power them.
