---
type: source
title: "Amazon's Trainium Takes a Strike at the Training King"
tags: [trainium, custom-silicon, pytorch, profiler, cuda-moat, aws]
related: ["[[semianalysis]]", "[[AMZN]]", "[[NVDA]]", "[[custom-silicon-asic]]", "[[ai-accelerator-competition]]", "[[geopolitics-export-controls]]"]
created: 2026-10-26
updated: 2026-10-26
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/amazons-trainium-takes-a-strike-at"
venue: SemiAnalysis
post_date: 2026-10-23
tickers: [AMZN]
---
A hands-on review (SemiAnalysis engineers ran Trainium3 racks for two weeks) arguing **Amazon has made a major software course-correction that will broaden Trainium3 beyond inference into research training.** Trainium was always great for inference (slow-moving architectures) but fell short for training's broad API surface. The fix is **TorchNeuron — a first-class native-PyTorch experience** replacing the old PyTorch/XLA lazy-graph duct tape: swap `.to("cuda")` for `.to("neuron")`, eager mode + `torch.compile`, native `torch.distributed`/DTensor/FSDP. AWS hired Google's native-Torch-on-TPU lead to build it.

Key findings:
- **Ecosystem breadth:** already supports Hugging Face Accelerate/Transformers/PEFT/TRL + TorchTitan (the popular Tier-2 pre-training base) + gpt-oss recipes; investing in vLLM/SGLang (the day-0 open-model engines) via TorchNeuron.
- **TorchTitan run:** Qwen3-32B on 16 Trainium2 → 23.89% MFU eager / **30.47% MFU compiled** (1.28× speedup); architecture edits "worked great." Rough edge: **Neuron compiler is slow** — first step 184-255s; gpt-oss took **27 min to compile** (historically inference-focused, compile cached offline). Next TorchNeuron targets ~2-orders-of-magnitude faster time-to-first-step.
- **MatMul:** a single Trainium3 logical core beats **GB300** MFU from the mid-range (1 GFLOP), GB300/B200 lead 100 GFLOP–1 TFLOP, **Trainium3 wins again past 1 TFLOP**.
- **FlexAttention:** 89/96 cases pass (93%); all 7 fails were compile-time-budget, not numerics.
- **QA culture:** up to **80k physical cores** on CI (vs "fighting tooth and nail" at other vendors); tests the top 100k+ HF models for numerics vs CPU/Nvidia; transparent internal parity tables (contrast: one vendor's leadership saw 99.99% while real gating parity was <5%).
- **Neuron Explorer profiler = SOTA**, "GPU-impossible": per-HW-unit event timeline, dependency coloring, even pixel-art from DMA engines; **Anthropic's head of performance publicly prefers it to Nvidia/AMD**. (Codex wrote the setup "since Claude refuses to write Trainium kernels.")

## Calls
- **LONG [[AMZN]]** ($248.00) — Trainium3's native-PyTorch stack + SOTA profiler + competitive MatMul materially broaden adoption; "nowhere near CUDA maturity, but the direction is right." Competitive read-through vs **[[NVDA]]** (profiler + mid-range MatMul lead; no fresh NVDA call). (→ [[custom-silicon-asic]], [[ai-accelerator-competition]])
