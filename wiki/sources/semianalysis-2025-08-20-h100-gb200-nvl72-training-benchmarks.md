---
type: source
title: "H100 vs GB200 NVL72 Training Benchmarks - Power, TCO, and Reliability Analysis, Software Improvement Over Time"
tags: []
related: []
created: 2025-08-20
updated: 2025-08-20
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/h100-vs-gb200-nvl72-training-benchmarks"
venue: SemiAnalysis
post_date: 2025-08-20
tickers: [NVDA]
---

[[semianalysis]] benchmarks NVIDIA H100 vs GB200 NVL72 for large-scale training, presenting detailed TCO, power, reliability, and software maturation data as of August 2025.

**TCO and Capital Costs.** An H100 server runs ~$190k, or ~$250k all-in with infrastructure. A GB200 NVL72 rack costs $3.1M, ~$3.9M all-in — roughly 1.6–1.7x the per-GPU capex of H100. GB200 consumes ~1,200W per chip versus ~700W for H100, but operating costs per GPU are not substantially higher. The GB200 therefore needs to deliver at least 1.6x the training throughput of H100 to achieve parity on performance-per-TCO.

**Software Improvements on H100 (Jan–Dec 2024).** GPT-3 175B training on 128 H100s: BF16 MFU improved from 34% to 54% (+57%); FP8 MFU from 29.5% to 39.5% (+34%). FP8 cost per million tokens fell from $0.72 to $0.542; training 300B tokens dropped from $218k to $162k. Drivers include improved fused wgmma kernels and optimized NCCL collectives consuming fewer SMs.

**Scaling and Model Benchmarks.** Llama 3 405B across 576–2,304 H100s sustains ~43% FP8 / ~54% BF16 MFU consistently, at $1.95/million tokens BF16 — consistent with Meta's published 41% BF16 MFU at 16k H100s. Llama 3 70B FP8 MFU drops ~10% scaling from 64 to 2,048 GPUs, while BF16 MFU is nearly flat. Training 15T tokens of Llama 3 405B costs ~$29.1M and consumes energy equivalent to ~3,400 US households annually.

**GB200 NVL72 Reliability.** As of August 2025, no large-scale training runs have been completed on GB200 NVL72. Even frontier labs and CSPs cannot yet execute mega training runs. The NVLink copper backplane remains unreliable even after extensive burn-in. Diagnostic and debugging tooling is described as behind and sub-optimal. The report expects software to improve considerably before year-end.

**Recommendations to NVIDIA.** (1) Expand public benchmark transparency across hyperscalers and NCPs — GCP's a3-mega H100 ran 10–20% worse MFU than average. (2) Prioritize PyTorch/FSDP2 over NeMo-MegatronLM — more NVIDIA engineers should contribute to PyTorch core. (3) Accelerate GB200 diagnostics and enforce stricter ODM/OEM acceptance testing.

## Calls

- [[NVDA]] — MENTION — px@n/a — GB200 NVL72 faces unresolved backplane reliability issues and immature software, delaying large-scale training deployments; H100 remains the proven workhorse but software gains are compounding its competitiveness.
