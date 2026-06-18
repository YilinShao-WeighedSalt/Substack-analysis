---
type: source
title: "Google TPU v8 Deep Dive: Precise Calculation of Optical, Copper, and PCB Requirements in Boardfly Topology"
tags: []
related: []
created: 2026-04-29
updated: 2026-04-29
authors: [globalsemiresearch]
year: 2026
url: "https://globalsemiresearch.substack.com/p/google-tpu-v8-deep-dive-precise-calculation"
venue: Global Semi Research
post_date: 2026-04-29
tickers: []
---

[[globalsemiresearch]] provides a detailed technical breakdown of Google's TPU v8 generation, announced at Cloud Next in April 2025, covering both the TPU 8t (Zebrafish) training chip and TPU 8i (Sunfish) inference chip — the first time Google has fully separated training and inference silicon.

**Compute vs. Bandwidth Shift**: The headline finding is that TPU v8 represents a strategic pivot from single-chip compute density to inter-chip communication bandwidth. TPU 8t compute is roughly comparable to v7; TPU 8i is dual-die but inference-targeted. The meaningful generational leap is at the network layer: TPU 8t DCN bandwidth increases 4× from 100 Gb/s to 400 Gb/s, supporting pods of up to 134,000 chips. TPU 8i's Boardfly topology cuts network diameter from 16 hops to 7 hops, a 56% reduction in latency.

**TPU v7 Ironwood Baseline**: To anchor the analysis, the post benchmarks v7 Ironwood: a 9,216-chip pod delivering 42.5 ExaFlops FP8, with 192 GB HBM3e per chip at 7.4 TB/s memory bandwidth. v7 uses a 3D torus ICI topology (4×4×4 Cubes, 64 TPUs each, 144 Cubes per full pod) with maximum intra-pod hop count of 6.

**Interconnect Material Mix (v7)**: The post derives precise per-chip ratios of optical fiber, copper cable, and PCB trace usage based on node position within the 3D torus Cube. Internal nodes (8 units) use 4 copper + 2 PCB; corner nodes (8 units) use 3 optical + 1 copper + 2 PCB; edge nodes (24 units) use 2 optical + 2 copper + 2 PCB; surface nodes (24 units) use 1 optical + 3 copper + 2 PCB. The normalized ratio across the full pod is TPU : PCB : Copper : Optical = 1 : 1 : 1.25 : 1.5. This framework is then applied to the v8i Boardfly topology to compute optical transceiver, copper cable, PCB, and OCS switch consumption — a supply-chain relevant calculation for vendors serving Google's AI infrastructure buildout.

**Strategic Implication**: As model training scales to hundreds of thousands of chips and inference demands low-latency sharding, bandwidth is the binding constraint. The shift to Boardfly topology in v8i (with OCS switches) signals growing demand for optical interconnect components across Google's data center fleet.

## Calls

No specific tickers are expressed with a directional view in the accessible portion of this post.
