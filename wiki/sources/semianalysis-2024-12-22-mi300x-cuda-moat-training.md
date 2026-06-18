---
type: source
title: "MI300X vs H100 vs H200 Benchmark Part 1: Training - CUDA Moat Still Alive"
tags: []
related: []
created: 2024-12-22
updated: 2024-12-22
authors: [semianalysis]
year: 2024
url: "https://newsletter.semianalysis.com/p/mi300x-vs-h100-vs-h200-benchmark-part-1-training"
venue: SemiAnalysis
post_date: 2024-12-22
tickers: [NVDA, AMD]
---

[[semianalysis]] published this five-month independent benchmarking study of AMD's MI300X against NVIDIA's H100 and H200 across LLM training workloads, concluding that the CUDA moat remains intact despite AMD's superior hardware specifications on paper.

## Hardware Advantage vs. Software Reality

The MI300X holds substantial on-paper advantages: 1,307 BF16 TFLOP/s vs. H100/H200's 989 TFLOP/s, 5.3 TB/s memory bandwidth vs. 3.35 TB/s (H100) / 4.8 TB/s (H200), and 192 GB HBM vs. 80/141 GB. However, actual GEMM benchmarks tell a different story — MI300X delivers ~620 BF16 TFLOP/s vs. H100/H200's ~720 TFLOP/s (14% slower), and ~990 FP8 TFLOP/s vs. ~1,280 TFLOP/s (22% slower). The hardware advantage is entirely consumed by software immaturity.

## Critical Software Bugs

The ROCm/PyTorch stack on public release MI300X was riddled with production-blocking issues: Flash Attention backward pass ran at <20 TFLOP/s for months (slower than CPU), inconsistent GEMM library dispatch between hipBLASLt and rocBLAS, torch.compile rank errors, and FlexAttention lagging NVIDIA by 6 months with convergence bugs on arrival. AMD's proposed workaround — PYTORCH_TUNABLE_OPS — requires 1-2 hours of per-model GEMM tuning, introduces 25 GB+ HBM memory leaks (eliminating MI300X's capacity advantage), and has known segfaults. Only hand-crafted AMD engineering builds (5-hour compile time) approach H100 performance; public stable releases do not.

## Networking and Scale-Out Gap

MI300X's xGMI interconnect provides only 64 GB/s between GPU pairs vs. NVLink's 450 GB/s — a 7x deficit for tensor-parallel workloads. At 32-GPU scale, MI300X on RoCEv2 Ethernet runs all-reduce at ~50% of InfiniBand speed, and lacks NVIDIA's in-network SHARP reduction capability. AMD's RCCL team has access to fewer than 32 MI300X GPUs for R&D vs. NVIDIA's 11,000+ internal H100 cluster.

## Cost and Market Context

A 16,000-GPU MI300X Ethernet cluster offers ~40% capex savings vs. H100/H200 InfiniBand, but on a performance-adjusted TCO basis H100/H200 delivers better $/effective-petaflop with public software. AMD guided $4-5B datacenter GPU revenue for 2024; investor expectations had been $6-8B. The gap between hardware potential and software delivery is characterized as an organizational QA and resource allocation failure, not a fundamental engineering limitation. AMD engineers are described as capable but systemically under-resourced.

## Calls

- [[NVDA]] — LONG — n/a — CUDA ecosystem depth and software maturity sustain H100/H200 training performance lead over MI300X despite hardware disadvantage
- [[AMD]] — SHORT — n/a — MI300X fails to translate hardware specs into real training throughput; software immaturity and organizational gaps underpin missed revenue expectations
