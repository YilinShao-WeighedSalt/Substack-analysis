---
type: source
title: "Amazon's AI Self Sufficiency | Trainium2 Architecture & Networking"
tags: []
related: []
created: 2024-12-03
updated: 2024-12-03
authors: [semianalysis]
year: 2024
url: "https://newsletter.semianalysis.com/p/amazons-ai-self-sufficiency-trainium2-architecture-networking"
venue: SemiAnalysis
post_date: 2024-12-03
tickers: [NVDA, AMZN, MRVL, AVGO]
---

[[semianalysis]] provides a deep technical teardown of Amazon's Trainium2 custom AI silicon, arguing Amazon is a "distant second" to Google in custom AI chips, still heavily reliant on NVIDIA, and that its flagship 400,000-chip Project Rainier cluster for Anthropic offers less raw compute than a 100,000-chip GB200 deployment.

## Strategic Position

Amazon's prior silicon generations (Trainium1, Inferentia2) failed to compete for frontier model training. The $4B Anthropic investment effectively finances Project Rainier in Indiana — 7 buildings at 455MW IT power today, scaling to 1,040MW. Internal models (Titan, Olympus) have stalled, making external validation through Anthropic critical. AWS remains dependent on NVIDIA capacity for near-term demand.

## Trainium2 Hardware

Each chip delivers 667 TFLOP/s BF16 with 96GB HBM3e at 2.9 TB/s bandwidth (~500W). Arithmetic intensity is 225.9 BF16 FLOP/byte — deliberately lower than GB200 (560) and TPUv6e (300) — a design tradeoff favoring memory-bound inference and Mixture-of-Experts (MoE) workloads. The microarchitecture includes four specialized engines (Tensor, Vector, Scalar, GpSimd) plus dedicated collective communication cores that eliminate the compute-vs-communication resource contention present in NVIDIA GPUs.

Two SKUs exist: Trn2 (16-chip 2D torus, single server, 800 Gbit/s scale-out) and Trn2-Ultra (64-chip 3D torus across two racks, 200 Gbit/s scale-out). NeuronLinkv3 scale-up uses passive copper backplane (intra-server) and Astera Labs AEC cables (inter-server), avoiding optical transceivers and achieving ~100× lower link-flapping rates vs. optics. Scale-out (EFAv3) uses a top-of-rack topology with Marvell Teralynx white-box ToR switches and Broadcom Tomahawk4 leaf/spine, achieving 6.5µs packet latency.

## Software and Risk

PyTorch XLA support is legacy-burdened; JAX is positioned as the natural fit given shared static-graph compilation and torus topology. A notable gap — All-to-All collective support required for MoE models — was absent since 2022 and only recently remediated. Key risks: (1) single chip failure disables the entire 64-chip Trn2-Ultra torus domain; (2) frontier training on Trainium2 remains undemonstrated; (3) Anthropic is the only major training customer. Marvell supplies Teralynx switch ASICs as sole-source ToR silicon; Broadcom supplies leaf/spine. Astera Labs is the sole AEC cable supplier for inter-server scale-up.

## Calls

- [[NVDA]] — LONG — n/a — AWS remains "heavily reliant on NVIDIA capacity"; Trainium2's 400k-chip cluster delivers less raw FLOPS than 100k GB200s, reinforcing NVIDIA's lead in frontier training
- [[AMZN]] — NEUTRAL — n/a — Trainium2 shows meaningful architectural progress but frontier training is unproven and Project Rainier success depends on undemonstrated asynchronous training algorithms
- [[MRVL]] — MENTION — n/a — Sole supplier of Teralynx 6.4T/12.8T ASICs used in Trainium2 ToR white-box switches
- [[AVGO]] — MENTION — n/a — Broadcom Tomahawk4 powers all leaf/spine switching in Trainium2 EFAv3 scale-out fabric
