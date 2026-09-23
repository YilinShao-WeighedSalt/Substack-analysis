---
type: source
title: "Computation and Data Movement for Inference"
tags: [inference, moe, hbm, networking, orchestration, technical]
related: ["[[semianalysis]]", "[[hbm-memory]]", "[[serdes-high-speed-connectivity]]", "[[ai-accelerator-competition]]"]
created: 2026-09-23
updated: 2026-09-23
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/computation-and-data-movement-for"
venue: SemiAnalysis
post_date: 2026-09-21
tickers: []
---

An 11k-word technical/educational deep-dive on how **Mixture-of-Experts (MoE)** reshaped inference serving economics — no priced ticker call. Feeds the concept layer.

- MoE changed *which tensors are active per token*, what must stay physically close, which transfers need strong local bandwidth vs. can tolerate weaker links, and how memory/storage/scheduling contribute to useful throughput.
- Serving is coordinated by orchestration (NVIDIA **Dynamo**, Mooncake, custom) atop inference servers (vLLM, SGLang). A "turn" = request→answer; tool intercepts create more turns; the **KV cache** distills the session.
- **Prefill/midfill** reward organized parallelism + stage-local expert traffic; **decode** benefits from low-latency parallelism but peak throughput/GPU comes from simpler attention + wide expert placement.
- **Key thesis-level conclusion:** across projected frontiers, **fast-memory *capacity* appears LESS restrictive than network placement, memory *bandwidth*, and orchestration.** → reinforces the running *bandwidth > capacity → 4-hi HBM* read ([[hbm-memory]]) and the *network wall* as the binding inference constraint ([[serdes-high-speed-connectivity]]).
- Framing: the useful unit of analysis is not total parameter count but the **active flow** joined to the memory/communication/timing hierarchy; the model, worker, rack, storage system, and scheduler become one coherent design.

## Calls
- None (technical/educational).
