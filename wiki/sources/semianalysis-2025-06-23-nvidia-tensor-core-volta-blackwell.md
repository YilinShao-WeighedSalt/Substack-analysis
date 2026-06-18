---
type: source
title: "NVIDIA Tensor Core Evolution: From Volta To Blackwell"
tags: []
related: []
created: 2025-06-23
updated: 2025-06-23
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/nvidia-tensor-core-evolution-from-volta-to-blackwell"
venue: SemiAnalysis
post_date: 2025-06-23
tickers: [NVDA]
---

[[semianalysis]] delivers a deep technical history of NVIDIA's Tensor Core architecture across five GPU generations — Volta, Turing, Ampere, Hopper, and Blackwell — tracing how hardware design choices were driven by the fundamental economics of data movement versus compute.

**Core thesis: data movement, not arithmetic, is the bottleneck.** An instruction fetch costs ~30pJ while an actual FP multiply costs ~1.5pJ — a 20x gap. Tensor Cores exist to amortize this overhead by executing large fused matrix-multiply-accumulate (MMA) operations per instruction. This framing underpins every design decision across generations.

**Volta (2017)** introduced the first Tensor Cores with `HMMA` instructions performing 8×8×4 matrix operations at the quadpair (8-thread) granularity, operands sourced entirely from registers.

**Ampere** added `cp.async` for direct global-to-shared memory transfers, eliminating register bounce and cutting register pressure. It also introduced `ldmatrix` and moved MMA to warp-level (32-thread) granularity, improving programmer ergonomics.

**Hopper** introduced thread block clusters and SM-to-SM shared memory transfers at low latency. The Tensor Memory Accelerator (TMA) enabled bulk asynchronous copies. Warpgroup-level asynchronous MMA (`wgmma`) operates across 128 threads and supports wide shape configurations (m64nN, N=8–256). FP8 formats (E4M3, E5M2) debuted, with accumulation over 22-bit fixed-point.

**Blackwell** is the most radical redesign. A new 256KB Tensor Memory (TMEM) replaces register-based operand staging, reducing register file pressure for the D matrix (read 2Kt times vs. once for A and B). CTA pairs share TPC resources across two CTAs, and MMA is now invoked by a single thread (`tcgen05.mma`). Shared memory capacity did not increase because MMA.2SM effectively pools two SMs' shared memory. Blackwell added microscaling formats (MXFP8/6/4) and proprietary NVFP4. Notably, FP8 and FP6 share physical circuits due to silicon area constraints — a different tradeoff than AMD's CDNA4, which shares FP6 with FP4.

**Structured sparsity critique.** The authors are sharply critical of NVIDIA's marketing of 2:4 sparsity as a throughput doubler. Despite theoretical 2× gains on Ampere and Hopper, real-world inference sees negligible uplift due to accuracy degradation from pruning and immature cuSPARSELt libraries. The piece directly calls on NVIDIA to stop citing structured sparsity peak-FLOPS in keynotes unless SOTA open models (including Llama variants being tested at Meta) consistently benefit. Blackwell's 4:8 pairwise NVFP4 sparsity faces the same practical constraint.

**Scaling rationale.** NVIDIA grew Tensor Core size faster than core count because MMA arithmetic intensity scales as O(n³) while data movement scales as O(n²) — larger tiles are more efficient. Wave quantization (underutilization when problem size doesn't tile evenly) is the key cost.

## Calls

- [[NVDA]] — LONG — px@n/a — Five-generation Tensor Core trajectory demonstrates compounding architectural moats: hardware–software co-design, proprietary low-precision formats (NVFP4), and TMEM/TMA abstractions that widen the CUDA ecosystem gap versus AMD CDNA4 and Google TPU alternatives
