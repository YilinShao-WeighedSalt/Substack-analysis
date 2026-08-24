---
type: source
title: "AgentX — InferenceXv3: Does the CUDA Moat Hold Up in Agentic Inferencing?"
tags: [inference-benchmark, cuda-moat, agentic, nvidia, amd]
related: [[[semianalysis]], [[NVDA]], [[AMD]], [[ai-accelerator-competition]], [[ai-software-models]]]
created: 2026-08-24
updated: 2026-08-24
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/agentx-inferencexv3-does-cuda-moat"
venue: SemiAnalysis
post_date: 2026-08-24
tickers: [NVDA, AMD]
---

# AgentX — InferenceXv3: Does the CUDA Moat Hold Up in Agentic Inferencing?

SemiAnalysis open-sources **AgentX 1.0** (Apache 2.0) — the first fully open, multi-turn agentic-coding inference benchmark at **1M context**, added to InferenceXv3 alongside the old fixed-sequence scenarios (8k1k/1k1k/1k8k). Since the "Claude Code inflection point" (Nov 2025), long-context, multi-turn, tool-calling agentic traffic dominates production inference; in April 2026 OpenAI's *enterprise agentic* spend overtook ChatGPT. The old fixed-prefill/decode way of measuring hardware is now wrong. The matrix runs ~2 MW across 1000+ chips: MI355X, GB300/GB200 NVL72, B300, B200, MI325, MI300X, H200, RTX Pro (Rubin/TPU/MI455X arriving later). ~$3M dataset build, all open.

## The core read — CUDA moat still holds on agentic workloads

- Across frontier open models (**Kimi K3 2.8T, MiniMax M3 432B, Qwen3.5 397B, GLM 5.3 744B, DeepSeek V4**), **Nvidia beats AMD on realistic multi-turn agentic serving.** Examples: Qwen3.5 SGLang — Nvidia >20× better at 90 tok/s/user, *zero AMD competition*; GLM 5.3 — Nvidia up to 5× better cost-efficiency at 150 tok/s/user p90; MiniMax M3 — "Nvidia absolutely destroys all competitors."
- The moat is **software, not silicon**: Nvidia's Pareto points use aggressive **KV-offload to CPU DRAM** above concurrency 20; AMD's don't (GPU↔CPU transfer path weaker). AMD tuned only for short-context single-turn; long-context multi-turn was neglected. On vLLM every AMD backend for DCP/PCP is unsupported.
- **AMD is closing it fast**: MI355X + **ATOM** (AMD's TensorRT-LLM equivalent) is competitive in the *ultra-high-throughput/low-interactivity* corner (batch, long-running agents) and on some models matches B200 vLLM on perf/$ — but AI labs won't run ATOM in production (want upstream vLLM/SGLang). MI355X FP4 disaggregation reached InferenceX months behind Nvidia on DeepSeek-R1; by MiniMax M3 it landed **day-zero**. Big engineering-velocity improvement.
- Punchline: **"even if AMD compute were sold for free, cost per token would still be cheaper on Nvidia."** After Aug-21 vLLM optimizations, B200 perf/$ surpassed MI355X.
- SemiAnalysis positions itself as a multi-year AMD-software collaborator; an AgentX update with fresh AMD/Nvidia numbers lands in 3–4 weeks.

## Calls
- [[NVDA]] — NEUTRAL (moat-holds / favorable) — $214.72 — CUDA software moat intact on agentic inference; cheaper $/token on most frontier models even vs hypothetically free AMD.
- [[AMD]] — NEUTRAL — $473.25 — MI355X/ATOM closing the gap fast (M3 day-0), competitive only in ultra-high-throughput corner; upstream vLLM/SGLang still trails on realistic long-context agentic serving.

Educational/benchmark post — directional read, not a fresh buy/sell thesis.
