---
type: source
title: "Dissecting Nvidia Blackwell - Tensor Cores, PTX Instructions, SASS, Floorsweep, Yield"
tags: []
related: []
created: 2026-03-31
updated: 2026-03-31
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/dissecting-nvidia-blackwell-tensor"
venue: SemiAnalysis
post_date: 2026-03-31
tickers: [NVDA]
---

[[semianalysis]] publishes a deep-dive microbenchmarking study of Nvidia's Blackwell (SM100) datacenter GPU, authored by Kimbo Chen. The work reverse-engineers PTX and SASS instruction behavior on B200 hardware to establish practical speed-of-light bounds for kernel authors targeting Blackwell.

The most significant architectural departure from Hopper is the introduction of Tensor Memory (TMEM): MMA accumulator results are no longer owned implicitly by warps but must be explicitly managed through a new memory tier. The new `tcgen05` instruction family is issued by a single thread on behalf of an entire CTA, a fundamental change in programming model. A second major addition is TPC-scoped collaborative MMA and TMA (cta_group::2), allowing two SMs to execute a single large matrix multiply, which the authors call 2SM MMA.

Memory subsystem benchmarking shows asynchronous copy (LDGSTS) peaks at roughly 6.6 TB/s at 32 KiB in-flight with a baseline latency near 600 ns; the Tensor Memory Accelerator (TMA) reaches peak throughput later but scales further and achieves "1 / cluster_size" L2 bytes per SMEM byte for known access patterns through multicast. Distributed shared memory (DSMEM) peer throughput is significantly lower than local SMEM — roughly 11.5–16 bytes/clock versus 128 bytes/clock — and requires coalesced access patterns.

Tensor core throughput analysis finds that M=64 tiles reach only ~50% of theoretical peak while M=128 approaches 100%. SMEM-bandwidth becomes the binding constraint for small-N shapes with SS (shared-shared) layout; switching to TS (TMEM-shared) layout recovers near-peak performance across shapes. At four in-flight MMAs, throughput saturates at 78–80% speed-of-light; the largest N shapes sustain ~90% SoL. 2SM MMA delivers near-perfect 2x weak scaling and can exceed 2x for SMEM-bound shapes.

A key physical-architecture finding comes from reverse-engineering SM-to-GPC mapping. Manufacturing yield variation causes floorsweeps that break clean logical groupings: the physical distribution estimated per die is Die A [10,10,10,9] and Die B [9,9,9,5+3], with die-to-die latency penalties of approximately 300 cycles. The authors warn that kernels launched with cluster size equal to SM count can serialize execution if cluster size does not evenly divide GPCs, and recommend using preferred/fallback cluster sizes to guarantee full GPU utilization.

The post releases an open-source microbenchmarking repository, with B200 node access provided by Nebius and Verda. Future work is planned on TPU Pallas, Trainium NKI, and AMD CDNA4.

## Calls

- [[NVDA]] — MENTION — px@call: n/a — Post is a technical deep-dive that implicitly validates Blackwell's architectural complexity and GPU moat; no explicit buy/sell stance is expressed.
