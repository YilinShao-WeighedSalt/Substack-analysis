---
type: source
title: "SemiAnalysis — How GLM5.3 Sparse Attention Affects HBM Memory Usage"
tags: [sparse-attention, dsa, hbm, kv-cache, inference-economics, moore-threads]
related: ["[[semianalysis]]", "[[MU]]", "[[NVDA]]", "[[AMD]]", "[[hbm-memory]]", "[[ai-accelerator-competition]]", "[[ai-software-models]]", "[[serdes-high-speed-connectivity]]"]
created: 2026-09-29
updated: 2026-09-29
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/sparse-savings-persistent-demand-inside-glm53"
venue: SemiAnalysis
post_date: 2026-09-28
tickers: [MU, NVDA, AMD]
---

# SemiAnalysis — How GLM5.3 Sparse Attention Affects HBM Memory Usage

Technical deep-dive on Z.ai's GLM-5.x (744B total / 40B active MoE, DeepSeek Sparse Attention). Paywalled; full body served. **No fresh priced ticker** — thesis-reinforcing for the memory + accelerator arcs.

## Summary

- **Core memory takeaway (bullish for HBM demand):** sparse attention selects top-k tokens to cut the compute/bandwidth of the attention op, **but it does NOT reduce overall HBM *capacity* need** — top-k selection still requires the full context resident in HBM. To serve long context at high concurrency, SGLang's **HiSparse** offloads KV entries HBM→host DRAM as an LRU cache (layer-wise prefetch overlap). So the memory-capacity bottleneck persists; system design, not the attention math, sets real KV efficiency → reinforces *bandwidth > capacity → 4-hi HBM* and **DRAM-offload-wins** ([[hbm-memory]]) → [[MU]] read stays NEUTRAL-supportive.
- **Serving economics (InferenceX, Sep-28 AgentX snapshot):** at 150 TPS, **GB200 ≈ $0.044/M total tokens vs MI355X-ATOM $0.049** (~12% cheaper); **GB300** serves ~13,950 tok/s/GPU (+17.5% vs GB200) but its higher $/GPU-hr ($2.31 vs $1.86) offsets the throughput at that target. With a 2s TTFT cap, **MI355X-ATOM $0.0607 beats B200 $0.0666** (~9%); relax to 10s TTFT and **GB300-TRT-LLM $0.0451** wins (~26% below ATOM). Neither side owns a uniform cost win → [[NVDA]] leads on cost-at-latency, [[AMD]] competitive in throughput corners but **TTFT still weak on TileRT** ([[ai-accelerator-competition]]).
- **Architecture color:** DeepSeek Sparse Attention = lightning indexer (down-projected Q/K, ReLU, no softmax/value) + sparse MLA in MQA mode; IndexShare (1 indexer / 4 DSA layers) cuts indexer cache & FLOPs 75%, +1.5–1.8× throughput. GLM-5 uses **64 query heads** (half DeepSeek's), implying it's tuned for lower-arithmetic-intensity hardware — SA suspects **Moore Threads MTT S4000** (~128 FLOP/B), corroborated by GLM-5.3-Flash day-0 support (China-accelerator angle). Post-training: on-policy cross-stage distillation / parallel OPD, GRPO+IcePop+Clip-Higher, SAO (single-rollout GAE) for long-horizon RL, on `slime`.

## Calls
- No priced call — technical/codesign piece.
- [[MU]] — thesis-reinforcing NEUTRAL-supportive — sparse attention leaves the HBM capacity bottleneck intact; KV-offload to host DRAM is the workaround, not less HBM.
- [[NVDA]] — thesis-reinforcing — GB200/GB300 hold cost-at-latency leadership across most targets.
- [[AMD]] — thesis-reinforcing NEUTRAL — MI355X-ATOM competitive in throughput/tight-TTFT corners but TileRT TTFT still suboptimal.
