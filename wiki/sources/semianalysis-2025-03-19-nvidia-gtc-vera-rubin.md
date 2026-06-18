---
type: source
title: "NVIDIA GTC 2025 - Built For Reasoning, Vera Rubin, Kyber, CPO, Dynamo Inference, Jensen Math, Feynman"
tags: []
related: []
created: 2025-03-19
updated: 2025-03-19
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/nvidia-gtc-2025-built-for-reasoning-vera-rubin-kyber-cpo-dynamo-inference-jensen-math-feynman"
venue: SemiAnalysis
post_date: 2025-03-19
tickers: [NVDA, AMD, MRVL]
---

[[semianalysis]] provides a deep-dive analysis of NVIDIA's GTC 2025 announcements, framing the event around three converging scaling paradigms — pre-training, post-training, and inference-time scaling — and the resulting demand explosion for AI compute driven by reasoning models.

**Hardware Roadmap.** Blackwell Ultra (B300) raises FP4 throughput by over 50% vs B200, expands HBM3E capacity to 288GB across eight stacks, and introduces the CX-8 NIC at 800G bandwidth. The next-generation Vera Rubin GPU, on TSMC 3nm with two reticle-sized compute dies plus two I/O tiles, delivers ~50 petaFLOPs dense FP4 — more than 3x B300 — with 288GB HBM4 at 20.5 TB/s bandwidth and sixth-gen NVLink at 3.6 TB/s bidirectional. Rubin Ultra scales further to four compute dies, 1024GB HBM4E, and ~100 petaFLOPs. The 2027 Kyber rack rotates blades 90 degrees into a dense NVL576 (144 packages / 576 dies) configuration, with evidence of a potential NVL1152 doubling density again.

**Dynamo Inference Engine.** NVIDIA's new distributed inference framework introduces a Smart Router (prefill/decode load balancing absent in vLLM), a GPU Planner (autoscaling, MoE expert-lane reallocation), improved NCCL with 4x lower latency for small messages (directly pressuring AMD's RCCL maintenance burden), NIXL (InfiniBand GPU-Async to bypass CPU proxy threads), and NVMe KV-cache offload. DeepSeek-disclosed 56.3% KV-cache hit rates imply 50–60% efficiency gains for multi-turn deployments.

**Co-Packaged Optics (CPO).** NVIDIA announced first-gen CPO switches replacing discrete transceivers: Quantum X-800 3400 CPO (144×800G ports, H2 2025) and Spectrum-X CPO Ethernet (512×800G, H2 2026). For a 400,000-GPU Blackwell cluster, CPO reduces transceiver power from 10% to 1% of compute, yielding a 12% total cluster power saving. CPO also enables network flattening from three to two layers, and may enable scale-up beyond 576 GPUs.

**"Jensen Math" conventions identified.** The article flags three specification tricks inflating headline numbers: (1) FLOPs quoted with 2:4 sparsity rather than dense, (2) NVLink bandwidth cited bidirectionally (TX+RX summed), (3) GPU counts by compute dies not packages (Rubin's 72 packages = NVL144).

**Cost/demand dynamics.** Jensen characterizes himself as "Chief revenue destroyer" — Blackwell delivers 68x Hopper performance at 87% cost reduction; Rubin projects 900x improvement at 99.97% cost reduction. Jevons' Paradox applies: efficiency gains expand total consumption as reasoning models consume 20x more tokens and 150x more compute than base models.

**Competitive implications.** NVIDIA's rapid NCCL advancement compounds AMD's RCCL engineering disadvantage. Dynamo's enterprise-friendly packaging democratizes DeepSeek-style inference efficiency, accelerating displacement of open-source inference stacks (vLLM, SGLang) in production.

## Calls

- [[NVDA]] — LONG — px@n/a — Multi-year product roadmap (Rubin, Kyber, CPO, Dynamo) reinforces NVIDIA's silicon-to-systems integration moat as reasoning-model compute demand accelerates
- [[AMD]] — SHORT — px@n/a — NVIDIA's rapidly evolving NCCL stack compounds AMD's RCCL maintenance burden and widens the software/ecosystem gap
- [[MRVL]] — MENTION — px@n/a — CPO networking strategy and custom ASIC ecosystem are relevant competitive backdrop to NVIDIA's CPO switch announcements
