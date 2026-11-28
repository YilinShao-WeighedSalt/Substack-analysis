---
type: source
title: "SemiAnalysis — AWS Challenger: Trainium3 Inference and Microarchitecture Deep Dive"
tags: []
related:
  - "[[semianalysis]]"
  - "[[AMZN]]"
  - "[[NVDA]]"
  - "[[ALAB]]"
  - "[[custom-silicon-asic]]"
  - "[[ai-accelerator-competition]]"
  - "[[nvidia-gpu-platform]]"
  - "[[serdes-high-speed-connectivity]]"
created: 2026-11-28
updated: 2026-11-28
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/trainium3-inferencex"
venue: SemiAnalysis
post_date: 2026-11-27
tickers: [AMZN, NVDA, ALAB]
---

A ground-up microarchitecture + microbenchmark deep-dive (UBenchX, validated with AWS Annapurna's Trainium team) arguing Trainium3 is now a genuine cost-per-token challenger to Nvidia. Full body served despite the "only_paid" flag.

- **The headline investment read:** on **AgentX** (replays real coding-agent sessions), Trainium3 + PDS + vLLM delivers the best perf/$ TCO across the entire frontier **except Vera Rubin**, beating GB300, B300 and MI355X. At a p90 interactivity of 135 tok/s/user (typical OpenRouter speed), Trainium3 + vLLM yields a **73.5% profit margin vs GB300 + SGLang's 53%** (3-yr rental, Z.ai token pricing, 60% fleet utilization). The edge is cost, not raw speed — Trainium3 has only 17% of Blackwell Ultra's FP4 FLOPs and 61% of GB300's HBM bandwidth (4.9 vs 8.0 TB/s) but at ~30% the TCO, and only 144GB HBM/chip (half GB300) — the "Short King" thesis (4-Hi HBM is enough for inference). Lags on p90 TTFT (prefill is compute-bound). Nvidia's own dashboard shows **Vera Rubin NVL72 at 3.3× Trainium3's tokens/$**, so Nvidia keeps the frontier while its two biggest custom-silicon rivals now publish its own metric. → **LONG [[AMZN]]**; reinforces the moat-erosion read on **[[NVDA]]** (SA's structural short, no fresh NVDA call here).
- **Why the software follows the hardware:** Trainium3 = 8 NeuronCore-v4s, every 2 cores share an HBM stack; a node is 16 chips. Prefill runs as a 16-stage pipeline (layers cut across chips, collectives kept on-chip because all-to-all is slow off-chip); decode spreads one model copy across all 128 cores. The **Descriptor Generation Engine (DGE)** (≈ Nvidia TMA / AMD TDM) lets Trainium hit peak HBM bandwidth at small message sizes — "not possible on Nvidia GPUs." New NeuronCore-v4 features: microscaling (MXFP4/MXFP8) matmul with quad-MXFP8 (K=512, 4× throughput), row-tiling mode, and a VectorE exponential for FlashAttention. MXFP8 power-throttles hard (68.6% MFU); BF16/MXFP4 ~90%.
- **Profiler = the soft moat:** Trainium's profiler is "by far the industry leader / SOTA," and Anthropic's head of performance says analysis on Trainium beats Nvidia and AMD — a developer-experience edge that compounds adoption.
- **Interconnect:** gen1 racks use 160-lane **Astera (ALAB) Scorpio X** PCIe switches (dual switch plane, checkerboard latency); **Trainium3n** (gen2) uses 320-lane Scorpio X single-plane trays, giving 2.8× all-to-all bandwidth (big for MoE) and removing a switch hop. → component read-through for [[ALAB]] (no priced ALAB call). → [[serdes-high-speed-connectivity]].

## Calls
- [[AMZN]] — **LONG** @ 244.43 — Trainium3 best perf/$ on AgentX except Vera Rubin (2.28× GB300 per SA's X post); 73.5% profit margin vs GB300's 53% at 135 tok/s/user; SOTA profiler; "Short King" 4-Hi HBM validated
