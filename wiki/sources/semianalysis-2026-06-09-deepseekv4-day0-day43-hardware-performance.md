---
type: source
title: "DeepSeekV4 1.6T Day 0 to Day 43 Performance Over Time - Huawei, GB300 NVL72, MI355X, B200"
tags: []
related: []
created: 2026-06-09
updated: 2026-06-09
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/deepseekv4-16t-day-0-to-day-43-performance"
venue: SemiAnalysis
post_date: 2026-06-09
tickers: [NVDA, AMD]
---

[[semianalysis]] tracked DeepSeek V4's inference performance across multiple hardware platforms from Day 0 through Day 43 via the InferenceX initiative, revealing stark divergences in Day 0 readiness and software optimization velocity.

NVIDIA's CUDA stack was one of only two stacks with full Day 0 support for DeepSeek V4; the other was Huawei's CANN stack on the Ascend 950DT — a notable first since all prior DeepSeek releases had only NVIDIA CUDA working on Day 0. NVIDIA's GB300 NVL72 emerged as the dominant platform, achieving the lowest cost per million output tokens at $0.156 (at 50 tok/s/user, 8k input / 1k output) and top throughput across all interactivity levels with multi-token prediction enabled. B200 systems saw token throughput per megawatt rise from ~300k to nearly 500k tokens/s/MW between Day 0 and June 5th — a pure software gain with no hardware change.

AMD's MI355X started in a non-deployable state (1–2 tokens/user/second), with the SGLang team requiring kernel replacements and batching support fixes. By Day 26, AMD achieved over 100x throughput improvement — a significant catch-up, but the starting point underscores fragility of AMD's inference ecosystem. AMD's internal ATOM engine serves zero production tokens and diverted engineering focus from the more productive vLLM/SGLang path.

NVIDIA's TensorRT-LLM had a critical Day 0 bug: a hardcoded `FHC_HIDDEN = 4096` constant in `mhcFusedHcKernel.cu` was incompatible with DeepSeek V4's 7168 hidden size. NVIDIA engineers initially removed the error guard rather than extending support, corrupting hidden states for a week. The bug was eventually patched, but the episode highlights testing gaps.

Huawei's Ascend 950DT demonstrated architectural innovations: dual AI core masters (AIC for matrix, AIV for vector), a dedicated CCU communication engine that offloads collective ops without consuming AI Core compute, and metadata scheduling moved to AI CPU to reduce pipeline bubbles. These design choices enabled competitive Day 0 performance.

DeepSeek V4's architecture advances include Compressed Sparse Attention and Heavily Compressed Attention achieving 50x KV cache reduction at 1M context, and a MegaMoE fused kernel claiming 1.92x theoretical speedup over the naive kernel. Deterministic batch-invariant kernels support RL training reproducibility at some performance cost.

## Calls

- [[NVDA]] — LONG — px@n/a — GB300 NVL72 leads on cost efficiency and throughput; CUDA stack had Day 0 support and remains the baseline all other stacks chase; software improvements on B200 delivered ~67% throughput/MW gains as pure software gains
- [[AMD]] — MENTION — px@n/a — MI355X achieved 100x throughput improvement by Day 26 but started non-deployable; ATOM engine serves zero production tokens, reflecting ongoing inference ecosystem weakness relative to CUDA
