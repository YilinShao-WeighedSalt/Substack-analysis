---
type: source
title: "The GPU Cloud ClusterMAX Rating System | How to Rent GPUs"
tags: []
related: []
created: 2025-03-26
updated: 2025-03-26
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/the-gpu-cloud-clustermax-rating-system-how-to-rent-gpus"
venue: SemiAnalysis
post_date: 2025-03-26
tickers: [CRWV, NVDA]
---

[[semianalysis]] introduces the ClusterMAX™ rating system — the first independent GPU cloud benchmarking framework — covering over 100 providers across ~90% of the GPU rental market by volume. The system rates providers across five tiers (Platinum, Gold, Silver, Bronze, UnderPerform) on security, lifecycle management, managed orchestration, storage, networking performance, reliability, health checks, pricing, and NVIDIA/AMD technical partnerships.

**Market Context.** GPU rental prices have collapsed as supply outpaces demand. On-demand H100 pricing spans roughly $1.50–$2.99/GPU-hour depending on provider and contract terms. With Blackwell entering volume production, Hopper-class hardware faces accelerating price pressure. The market has shifted from scarcity to a buyer's market with "100+ GPU clouds all competing for mostly the same customers."

**Platinum: CoreWeave.** CoreWeave is the only Platinum-rated provider. Key differentiators include: automated node lifecycle controllers with comprehensive burn-in testing; continuous passive health monitoring for GPU bus errors, PCIe faults, and thermal events; weekly automated active health checks (DCGM diagnostics, NCCL tests, Silent Data Corruption detection); managed Slurm and Kubernetes with topology-aware scheduling; and InfiniBand SHARP in-network reduction — enabling 10,000+ GPU clusters. The report notes that OpenAI, Meta, and Jane Street all use CoreWeave's managed solutions despite having the in-house capability to build their own, which is treated as a strong third-party validation.

**Gold Tier.** Crusoe earns Gold for its newly launched "Auto Clusters" managed Slurm offering and strong white-glove service, though it lacks advanced active health checks. Nebius offers the lowest absolute pricing (~$1.50/hour for first 1,000 GPU-hours/month) via an ODM hardware strategy that compresses margins to ~2%, but has weak UI/UX. Oracle Cloud Infrastructure is called the most cost-effective hyperscaler, with one-click HPC stack deployment but no fully managed Slurm. Azure earns Gold on security and reliability (managing OpenAI's deployments), with InfiniBand SHARP, but trails CoreWeave on health-check automation. Together AI is elevated to Gold for proprietary kernel optimizations (Together Kernel Collection, authored by Flash Attention creator Tri Dao) that benefit ~30–40% of workloads.

**Security Gap.** Many providers lack SOC2 or ISO27001 certification. Kubernetes namespace isolation is flagged as inadequate given monthly container escape CVEs; proper tenant isolation requires VLANs, separate Kubernetes clusters, or VM-level isolation.

**Networking.** ConnectX-7 NICs perform best. InfiniBand SHARP yields superior bandwidth but only five customers globally use it in production. Topology-aware scheduling provides 20–30% performance uplift. SemiAnalysis calls on NVIDIA and AMD to mandate SOC2 for all cloud partners, improve InfiniBand security-key and SHARP documentation, and conduct hyperscaler NCCL regression testing.

## Calls

- [[CRWV]] — LONG — px@n/a — sole Platinum-rated provider; validated by OpenAI, Meta, and Jane Street adoption; strongest automation, health checks, and scale capabilities in the market
- [[NVDA]] — MENTION — px@n/a — recommended to mandate SOC2 for cloud partners and improve InfiniBand/SHARP tooling; no direct investment stance expressed
