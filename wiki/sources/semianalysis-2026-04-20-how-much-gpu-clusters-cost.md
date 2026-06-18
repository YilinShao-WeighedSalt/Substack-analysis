---
type: source
title: "How Much Do GPU Clusters Really Cost?"
tags: []
related: []
created: 2026-04-20
updated: 2026-04-20
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/how-much-do-gpu-clusters-really-cost"
venue: SemiAnalysis
post_date: 2026-04-20
tickers: []
---

[[semianalysis]] presents a comprehensive Total Cost of Ownership (TCO) framework for GPU clusters, arguing that headline GPU rental prices obscure the true cost of running AI workloads. The framework decomposes cluster costs into eight components: GPU rental, storage (hot/warm/cold tiers), networking (frontend and backend), control plane, support, goodput expense (downtime and interruption losses), setup costs, and ongoing debugging costs.

When GPU pricing is held equal across provider tiers, TCO differences range from 5–15% for large training workloads but approach zero for fault-tolerant single-node inference clusters. Three scenario analyses illustrate this concretely. For a large LLM pretraining job at 5,184 GPUs, a gold-tier neocloud (Nebius, Fluidstack, Crusoe) serves as the 1.0x baseline; hyperscalers (AWS, Azure, GCP, Oracle) run 1.10x and silver-tier neoclouds 1.15x, driven primarily by support costs and extensive network tuning overhead. For a 2,048-GPU multimodal RL research workload where GPU pricing diverges ($2.40/hr gold versus $3.10/hr hyperscaler), the hyperscaler premium widens to 1.61x. For 512-GPU inference endpoints, gold and silver tiers reach near parity while hyperscalers remain 1.59x more expensive.

A central concept is "goodput expense" — the economic cost of lost training progress from hardware failures. The analysis introduces three fault-tolerance regimes: checkpoint-cold restart (wait for provider repair), checkpoint-hot restart (restart on customer-managed spare nodes), and fully fault-tolerant training. Goodput losses for large pretraining range from 6.14% with TorchPass (Clockwork's zero-overhead migration tool) to 20.91% with silver-tier checkpoint restart. Meta's open-source TorchFT imposes over 10% performance overhead; AWS SageMaker HyperPod Checkpointless achieves ~1m45s recovery but carries ~5% memory overhead.

Storage is a frequently overlooked cost lever: AWS FSx Lustre throughput tiers range from 125 MB/s/TiB to 1,000 MB/s/TiB at a roughly 3x cost difference for 4x throughput. Hyperscaler support contracts add 3–10% bill uplift. Large pretraining on hyperscalers requires an estimated one-month paid POC plus two engineers one week per month for network debugging.

The ClusterMAX 2.1 update adds assessments of Core42 (UAE/US, praised for proactive support), BitDeer (Malaysia, early GB200 NVL72 testing), FPT Smart Cloud (Vietnam, strong monitoring but security gaps), and Radiant/Ori (Saudi Aramco-backed, missing automated health checks). Pricing data referenced from August 2025; GPU shortage since that period has pushed prices upward.

## Calls

No ticker-level investment stances are expressed in this post. The analysis is a technical TCO framework and provider benchmark, not a securities recommendation.
