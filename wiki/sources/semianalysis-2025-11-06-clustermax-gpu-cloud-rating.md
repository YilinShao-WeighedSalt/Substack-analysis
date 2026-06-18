---
type: source
title: "ClusterMAX 2.0: The Industry Standard GPU Cloud Rating System"
tags: []
related: []
created: 2025-11-06
updated: 2025-11-06
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/clustermax-20-the-industry-standard"
venue: SemiAnalysis
post_date: 2025-11-06
tickers: [CRWV, NVDA, AMD, ORCL, MSFT, GOOGL, AMZN, WULF, IREN, HUT, BTDR, APLD, CORZ, CIFR]
---

[[semianalysis]] presents ClusterMAX 2.0, an expanded industry benchmark rating 84 GPU cloud providers (up from 26 in v1.0) across 10 evaluation categories, having surveyed 140+ end users and tracked 209 total providers. The system has achieved broad institutional endorsement from OpenAI, Meta, and Dell, with rated neoclouds collectively booking nearly $400 billion in remaining performance obligations since the v1.0 release in March 2025.

## Tier Rankings

CoreWeave is the sole Platinum-tier provider, distinguished by its SUNK (SLURM-on-Kubernetes) architecture, DPU offloading via NVIDIA BlueField, bare-metal performance, and rack-level SLAs. Gold tier includes Nebius, Oracle, Azure, Crusoe, and Fluidstack. Silver tier covers Google, AWS, together.ai, and Lambda. Thirty-seven providers receive Bronze, and the remainder are rated Underperforming or Unavailable.

## Evaluation Framework

The ten categories are: Security (SOC 2/ISO compliance, InfiniBand multi-key isolation), Lifecycle (onboarding/offboarding), Orchestration (SLURM/Kubernetes hybrid), Storage (POSIX + S3-compatible), Networking (InfiniBand/RoCEv2, SHARP), Reliability (99.9% hardware SLA, automated remediation), Monitoring (Grafana/DCGM), Pricing (per-GPU-hour across contract terms), Partnerships (NVIDIA/AMD certifications), and Availability (GPU quantity and model freshness including H200, B200, MI300X). Key benchmarks include PyTorch install time, NGC container pull speed, and NCCL interconnect tests across multi-node training jobs.

## Technical Findings

GB200 NVL72 provisioning is a serious operational challenge: the entire 72-GPU rack is a single failure domain, recovering from failures requires 9 hours to multiple days and 9–14 provisioning steps, and firmware v1.3 (released November 2025) only now addresses NVLink sync stability issues present for six months. On security, the NVIDIAscape vulnerability (CVE-2025-23266) — a three-line container escape granting root access — affected over a dozen providers still running nvidia-container-toolkit below v1.17.8 during testing. Proper InfiniBand multi-tenant isolation requires layered keys (M_Key, P_Key, SA_Key, VS_Key, C_Key, AM_Key) that most providers misconfigure. AMD cloud offerings at hybrid providers (Crusoe, Oracle) are described as significantly inferior to their NVIDIA equivalents, lacking monitoring, health checks, and working SLURM support.

## NVIDIA DGX Cloud Criticism

NVIDIA's DGX Cloud strategy is criticized sharply: ~$2.1B in acquisitions (Lepton, run:ai, Deci, shoreline.io, brev.dev) has produced minimal public releases or open-source output. DGX Cloud Lepton is characterized as a "bring your own cloud" arrangement with no pre-registered providers. A100 pricing on Azure via DGX Cloud at $4.05/hour ($23,360/month per node) is cited as the worst observed pricing in the survey.

## Bitcoin Miner Pivot to AI

A notable theme is Bitcoin miners converting infrastructure to GPU cloud: Terawulf, Cipher Mining, IREN/Iris Energy, Hut 8, BitDeer, Applied Digital, and Core Scientific are all cited. IREN is highlighted specifically for a 200MW Microsoft deal for GB300 GPUs at Childress, TX, retrofitting an entire Bitcoin mine into a GPU cluster. Two models are identified: powered-shell colocation (renting datacenter space to neoclouds) and wholesale bare-metal GPU procurement using low energy cost advantages.

## Calls

- [[CRWV]] — LONG — n/a — sole Platinum-tier provider; SUNK architecture, bare-metal performance, and rack-level SLAs create durable competitive moat in enterprise GPU cloud
- [[NVDA]] — MENTION — n/a — InfiniBand security gaps and DGX Cloud strategy failure are structural negatives; ecosystem dominance remains but execution criticized
- [[AMD]] — MENTION — n/a — cloud quality gap vs. NVIDIA is significant; hybrid providers' AMD offerings lack monitoring, health checks, and SLURM support
- [[ORCL]] — MENTION — n/a — Gold-tier rating; competitive neocloud offering with bare-metal + DPU architecture
- [[MSFT]] — MENTION — n/a — Gold-tier (Azure) but hosts worst observed DGX Cloud A100 pricing at $4.05/hour
- [[GOOGL]] — MENTION — n/a — Silver-tier despite hyperscaler scale; storage and orchestration gaps noted
- [[AMZN]] — MENTION — n/a — Silver-tier alongside Google; behind specialized neoclouds on operational maturity
- [[WULF]] — MENTION — n/a — Bitcoin miner pivoting to AI GPU cloud via powered-shell colocation model
- [[IREN]] — MENTION — n/a — 200MW Microsoft GB300 deal highlights miner-to-AI conversion thesis; full mine retrofit underway
- [[HUT]] — MENTION — n/a — Hut 8/Highrise cited as Bitcoin miner pivoting to AI infrastructure
- [[BTDR]] — MENTION — n/a — BitDeer cited as miner pivoting to wholesale bare-metal GPU procurement
- [[APLD]] — MENTION — n/a — Applied Digital cited in Bitcoin miner AI pivot cohort
- [[CORZ]] — MENTION — n/a — Core Scientific cited in Bitcoin miner AI pivot cohort
- [[CIFR]] — MENTION — n/a — Cipher Mining cited in Bitcoin miner AI pivot cohort
