---
type: source
title: "AI Neocloud Playbook and Anatomy"
tags: []
related: []
created: 2024-10-03
updated: 2024-10-03
authors: [semianalysis]
year: 2024
url: "https://newsletter.semianalysis.com/p/ai-neocloud-playbook-and-anatomy"
venue: SemiAnalysis
post_date: 2024-10-03
tickers: [NVDA, SMCI, MSFT]
---
[[semianalysis]] (Dylan Patel and Daniel Nishball) presents a deep operational and economic blueprint for AI Neoclouds — the new class of GPU-rental cloud providers (CoreWeave, Lambda Labs, Crusoe, Nebius, and others) that have emerged to serve AI training and inference demand. The analysis spans cluster architecture, bill of materials (BoM) optimization, operational best practices, and partial economics.

On cluster architecture, the authors dissect a canonical 1,024-GPU H100 cluster and show where neoclouds can cut costs without sacrificing performance. A key insight is that the frontend network (client traffic) does not need expensive Nvidia Spectrum switches — generic 2×100GbE Ethernet suffices — while the backend InfiniBand fabric (GPU-to-GPU collective communications) should not be skimped on, with 8×400Gbit/s InfiniBand per node recommended. The proposed "virtual modular switch" topology achieves a 24.9% backend network cost saving vs. the reference design, and a 2:1 oversubscribed variant saves 31.6%, trading some flexibility for lower CapEx. Other BoM savings include downgrading CPUs (~$3k/node), reducing RAM from 2 TB to 1 TB (~$5k/node), and eliminating Nvidia BlueField-3 DPUs (~$5.6k/node), for roughly $13.6k (5%) savings per server. Avoiding Nvidia AI Enterprise licensing (~$4,500/GPU/year) is flagged as a significant opex lever.

Operationally, the post stresses that proper driver configuration (GPUDirect RDMA + Nvidia HPC-X) is critical — misconfiguration can drop GPU-to-NIC bandwidth from 391 Gbit/s to 80 Gbit/s. Storage deployments from Weka and Vast Data are recommended for multi-tenant shared filesystems. Scheduler mix among enterprise customers is ~70% SLURM, 20% Kubernetes, 10% custom. Reliability at top-tier operators (Crusoe, TogetherAI) averages ~7-day mean time between failures for 512-GPU clusters, with TogetherAI differentiated by exclusive Flash Attention CUDA kernels (Tri Dao) providing 10–15% training speedups. Neoclouds that skip proper multi-week burn-in see "orders of magnitude worse" reliability.

On market structure, Microsoft alone is spending roughly $200M/month on neocloud GPU compute despite its own datacenter capacity, validating the market size. Neoclouds are projected to represent more than a third of total AI compute demand. H100 on-demand pricing has seen "rapid declines" in the near term, while Blackwell deployment will further reshape the competitive landscape. Part 2 (paywalled) covers TCO, margins, and pricing dynamics in detail.

## Calls

- [[NVDA]] — MENTION — n/a — InfiniBand backend, H100 GPUs, and NVLink fabric are the core infrastructure layer for all neoclouds; licensing fees represent a significant margin lever for neoclouds seeking to avoid Nvidia's software stack
- [[SMCI]] — MENTION — n/a — Cited alongside Dell as a primary OEM for neocloud server deployments; BoM optimization examples reference Supermicro chassis configurations
- [[MSFT]] — MENTION — n/a — Highlighted as spending ~$200M/month on neocloud GPU compute despite internal Azure capacity, illustrating hyperscaler reliance on neoclouds and validating demand scale
