---
type: source
title: "CPUs are Back: The Datacenter CPU Landscape in 2026"
tags: []
related: []
created: 2026-02-09
updated: 2026-02-09
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/cpus-are-back-the-datacenter-cpu"
venue: SemiAnalysis
post_date: 2026-02-09
tickers: [INTC, AMD, NVDA, AVGO, ARM]
---

[[semianalysis]] argues that CPUs are experiencing a structural resurgence inside AI datacenters after years of GPU-driven eclipse, driven by reinforcement learning training loops, agentic systems, and petabyte-scale data management — all workloads that require large, parallel CPU clusters co-located with GPU arrays.

## The CPU Demand Thesis

RL training loops depend on CPUs for code compilation, verification, physics simulations, and tool execution. The "RL Environment" component must run fast enough to prevent GPU idle time, requiring dedicated CPU clusters adjacent to GPU arrays. Beyond training, agentic models with API integrations and RAG retrieval generate substantially more general-purpose compute demand. CPUs also shoulder data pipeline work — petabyte-scale sharding, indexing, and preprocessing — that would not exist without AI scaling.

## Intel Diamond Rapids: A Stumble

Diamond Rapids ships with four Core Building Block (CBB) dies plus two I/O Memory Hub dies, for 256 total cores (192 enabled). Intel eliminated SMT (Simultaneous Multi-Threading) on P-cores — citing Spectre/Meltdown mitigations — reducing effective throughput by roughly 40% versus AMD equivalents in multi-threaded workloads. Cross-die communication without EMIB advanced packaging introduces meaningfully worse core-to-core latencies (a trajectory already visible from 47 ns at Skylake to 59 ns at Sapphire Rapids). Intel also cancelled mainstream 8-channel Diamond Rapids-SP entirely, ceding that segment. Performance improvement over Granite Rapids is only ~40% over a two-year gap.

## AMD Venice: Taking Share

Venice delivers 256 Zen 6 cores with a new 32-core CCD (4×8 mesh layout), 16-channel DDR5, and Multiplexed MRDIMM support reaching 1.64 TB/s bandwidth — a 2.67× improvement over Turin. AMD adopts advanced interconnect packaging (EMIB-equivalent) for better coherence and adds new instructions including AVX512_FP16, AVXVNNI_INT8, and AVX512_BMM (Bit Matrix Multiplication) targeting AI pre/post-processing. AMD guides for "strong double-digit" datacenter CPU growth in 2026 with continued share gains. An 8-channel SP8 platform targets enterprise consolidation, where socket ratios of 10:1+ are possible.

## Hyperscaler Custom ARM and NVIDIA Vera

AWS Graviton5 (192 cores, 3 nm), Microsoft Cobalt 200 (132 cores, 50% speedup), Google Axion, and Meta's ARM Phoenix deployment all represent vertical integration reducing merchant silicon TAM. NVIDIA's Vera CPU (Rubin-paired, 88 custom Olympus cores with SMT, 1.8 TB/s C2C bandwidth, 1.5 TB addressable memory) is a direct response to Grace's L2 cache and bandwidth limitations. Ampere Computing was acquired by SoftBank in 2025 for $6.5 B. Huawei's Kunpeng 950 (192 cores, 12-channel DDR5) targets the Chinese captive market on SMIC N+3, constrained to 5-year generation gaps by US sanctions.

## Power and Memory Dynamics

Microsoft's "Fairwater" datacenter illustrates the emerging CPU power constraint: a 48 MW CPU building supports a 295 MW GPU cluster. As GPU efficiency improves faster than CPU efficiency, the CPU-to-GPU power ratio becomes a binding bottleneck. Venice's 1.64 TB/s memory bandwidth versus Turin's 614 GB/s is a critical evolution for data-intensive AI preprocessing.

## Calls

- [[INTC]] — SHORT — n/a — Diamond Rapids cedes ~40% throughput versus AMD via SMT removal; cancelled SP platform, latency regressions, and minimal performance uplift signal continued share loss
- [[AMD]] — LONG — n/a — Venice's core count, bandwidth, and packaging advantages position it to capture datacenter CPU share from Intel as AI-driven CPU demand inflects upward
- [[NVDA]] — LONG — n/a — Vera CPU entry with custom Olympus core and massive C2C bandwidth extends NVIDIA's full-stack datacenter control into CPU territory
- [[AVGO]] — MENTION — n/a — networking silicon competes for advanced node capacity alongside CPU silicon in the AI datacenter build-out
- [[ARM]] — LONG — n/a — hyperscaler custom ARM deployments (Graviton5, Cobalt 200, Axion, Phoenix) drive royalty growth as ARM architecture displaces x86 in cloud CPU sockets
