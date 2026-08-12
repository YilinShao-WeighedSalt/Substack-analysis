---
type: source
title: "Ultra-High Interactivity on NVIDIA GPUs? — TileRT InferenceX"
tags: [inference, gpu, cerebras, groq, sambanova, tilert, ai-hardware]
related: ["[[semianalysis]]", "[[CBRS]]", "[[NVDA]]", "[[ai-accelerator-competition]]", "[[ai-software-models]]"]
created: 2026-08-12
updated: 2026-08-12
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/ultra-high-interactivity-on-nvidia"
venue: SemiAnalysis
post_date: 2026-08-10
tickers: [CBRS, NVDA]
---
Educational deep-dive with a structural read-through for inference-ASIC vendors. **TileRT** statically compiles the entire decode graph into one *persistent* GPU kernel (vs CUDA graphs, which still launch separate kernels), with warp/GPU-level specialization and overlapped compute↔comms. On a single 8-GPU B200 node it reaches ~340–500 tok/s/user at BS1 — up to ~3× GB300 NVL72 interactivity — trading aggregate throughput for per-user speed (single in-flight request per decode node). Already in production behind Xiaomi MiMo and Z.ai GLM-5.1 HighSpeed. Composes with vLLM via PD-disaggregation (vLLM keeps prefill/API; TileRT takes latency-critical decode).

**Why it pressures specialist chips (Cerebras/Groq/SambaNova):** it reframes ultra-low-latency as a *speed tier* provisioned dynamically out of a fungible GPU fleet, not a chip you must buy and rack for months. "Good enough on hardware you already own beats architecturally pure on hardware you have to buy." Caveats: the SRAM roofline is still better (Cerebras serves dense 70B at speeds no 8-GPU node can match); TileRT's model catalog is tiny (GLM-5/5.1, DeepSeek-V3.2) with heavy per-model compile effort — the same weakness ASIC compilers have. Net: not a killer, but a real TAM headwind for the inference-ASIC pure-plays.

## Calls
- [[CBRS]] NEUTRAL $234.76 — TileRT reframes speed as a rentable tier; structural inference-ASIC TAM pressure (read-through)
