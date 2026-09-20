---
type: source
title: "Engrams Embedding Entendre: Codesign for Efficient DRAM/SSD Offloading"
tags: [hbm, cuda-moat, inference, memory-offload, deepseek]
related: [semianalysis, NVDA, AMD, MU, hbm-memory, ai-accelerator-competition, custom-silicon-asic]
created: 2026-09-20
updated: 2026-09-20
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/engrams-embedding-entendre-codesign"
venue: SemiAnalysis
post_date: 2026-09-18
tickers: [NVDA, AMD, MU]
---

# Engrams Embedding Entendre — Codesign for Efficient DRAM/SSD Offloading

Technical deep-dive tying DeepSeek's **Engram** architecture to memory-tier offloading
and the latest **InferenceX** agentic-serving results. A codesign / CUDA-moat piece more
than a fresh thesis, but it sharpens two running arcs: the **HBM de-spec** ([[hbm-memory]])
and the **CUDA moat** ([[ai-accelerator-competition]]).

## What Engram is
- **Engram** extends token embeddings with learned multi-token lookups: recurring local
  patterns retrieve vectors directly, reducing reconstruction through attention/FFN. Net
  effect — **lower HBM *capacity* needed for equal model quality.**
- Naturally codesigned for **parameter offloading**: each token accesses a few embedding
  rows whose addresses depend on token IDs (not hidden states), so the runtime can
  **prefetch rows from host DRAM** while earlier layers compute — table lives outside HBM.
- Ties directly to the Rubin Ultra de-spec (HBM/chip cut from ~1024GB → ~200GB): model
  architecture keeps innovating *around* memory constraints. "Does not mean HBM demand
  falls" — but it means **bandwidth matters more than capacity → 4-hi HBM = best
  $/bandwidth → lowest $/token.** (SA half-jokes China innovation could reach "0-hi HBM.")

## Offloading experiments (DeepSeek-V4.1-Flash, ~189 GiB Engram table)
- **DRAM offload wins:** on B300, Engram-to-DRAM lets you drop TP4→TP2 (fewer HBM GPUs
  per replica), improving the pareto **up to 1.6×**; moving the table back into HBM barely
  helped (within run-to-run variance) while consuming KV-cache space.
- **SSD offload loses:** on B200, memory-mapped SSD Engram tables are dominated by DRAM on
  both P90 interactivity and tokens/$ (near 125 tok/s/user: DRAM 121M vs SSD 52M total
  tokens/$). "Cheaper storage does not automatically produce a cheaper inference service" —
  the four expensive GPUs stay in place. Not worth it in production (current unoptimized path).
- **Removing Engram** degrades likelihood across domains (esp. encyclopedia/code); factual
  benchmarks retained only 29–44% in the paper's ablation. Memory + expert selection work
  together (not "memory stores facts, experts reason").

## CUDA moat (InferenceX, Day-0 of DeepSeek-V4.1-Flash)
- **NVIDIA vLLM works out-of-the-box day-0 across all 6 SKUs** (H100/H200/B200/B300/GB200/GB300).
- **AMD vLLM did NOT work day-0**; AMD's documented image wasn't public through hour 23.
  When released, perf was **up to 14.8× worse perf/$ than H200, up to 42× worse than
  B200/B300** at first; after optimization **still ~2–4× worse perf/$ than B200** even
  TCO-normalized on MI355X. "SPEED IS THE MOAT" — yet AMD missed hour-0.
- InferenceX now spans TPUv7, Jalapeño, Rubin NVL72, AMD (+SambaNova/Trainium soon);
  AMD committed to collaborating on MI455X UALoE72.

## Calls
- **[[NVDA]] LONG** — CUDA moat reaffirmed on the hottest open model; day-0 vLLM across all
  SKUs; MI355X still 2–4× behind. px@call $222.27.
- **[[AMD]] NEUTRAL** — real improvements but 2–4× worse perf/$ vs B200 and a botched
  day-0 image; "kernel/software process" still the gap. px@call $559.82.
- **[[MU]] NEUTRAL** — Engram cuts HBM *capacity* need (offload to DRAM), but bandwidth >
  capacity keeps HBM demand and pushes 4-hi; not a clean short. px@call $1,015.80.
