---
type: source
title: "SA: The Iron(wood) Throne — TPUv7 beats GB300 on perf-per-$ in agentic inference"
tags: []
related: ["[[GOOGL]]", "[[NVDA]]", "[[AMD]]", "[[AVGO]]", "[[custom-silicon-asic]]", "[[ai-accelerator-competition]]", "[[nvidia-gpu-platform]]", "[[semianalysis]]"]
created: 2026-11-07
updated: 2026-11-07
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/tpu-strikes-the-king"
venue: SemiAnalysis
post_date: 2026-11-05
tickers: [GOOGL, NVDA, AMD, AVGO]
---

SA's follow-up to its Sept TPU-externalization call: Google's **TPUv7 "Ironwood"** now posts official long-context, multi-turn **AgentX** results across four open models and is **competitive-to-best on tokens-per-dollar for external customers**. Highlights: on **GLM-5.2 FP8** TPUv7 is the cheapest option (1.2-2.7x the tokens/$ of B200/B300/MI355X); on **Qwen3.5 397B FP8** with llm-d it beats GB300 FP8 at every interactivity and 1.67x better per-$ than even FP4 GB300; on **Kimi K3** competitive with GB300 at launch; on Meta's GPU-optimized **Muse Spark Open** (head_dim 64 pads 25% of the systolic array) still competitive. Caveats: NVIDIA's FP4 refreshes reclaim decode lead on some models (overtuned prefill though → TPU FP8 still wins end-to-end on several), **TPUv7 has no native FP4** until TPUv8 (Q1-27), and Rubin NVL72 preview is ~4-6x better per-$ (unfair vs TPUv8i, benchmarking soon). The bigger thesis: TPU is applying NVIDIA's own ecosystem playbook (chips to vLLM/SGLang/PyTorch/llm-d maintainers; Day-0 model support), while **NVIDIA's bureaucracy** (3-month legal reviews on driver features, stingy OSS cluster access) is slowing it vs AMD/Google — SA's named "biggest risk to the NVIDIA moat." External TPU customers now include Oracle/OpenAI/Anthropic/Meta.

## Calls
- **[[GOOGL]] LONG** — TPUv7 competitive-to-best perf-per-$ in realistic agentic inference; ecosystem + external-customer traction.
- **[[NVDA]] NEUTRAL** — still leads on Rubin/FP4 but perf-per-$ moat eroding; bureaucracy a structural risk. No fresh short.
- Read-through: **[[AVGO]]** (TPU co-design), **[[AMD]]** (cited as fast-moving on megakernels/OSS).
