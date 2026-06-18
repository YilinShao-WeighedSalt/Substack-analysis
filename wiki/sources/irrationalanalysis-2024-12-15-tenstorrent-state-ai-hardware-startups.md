---
type: source
title: "Tenstorrent and the State of AI Hardware Startups"
tags: []
related: []
created: 2024-12-15
updated: 2024-12-15
authors: [irrationalanalysis]
year: 2024
url: "https://irrationalanalysis.substack.com/p/tenstorrent-and-the-state-of-ai-hardware"
venue: Irrational Analysis
post_date: 2024-12-15
tickers: [NVDA, ARM, CBRS]
---

[[irrationalanalysis]] visited Tenstorrent's offices for a 1.5-hour technical deep-dive after a prior skeptical post on their Hot Chips 2024 presentation prompted an invitation from the company's Chief Customer Officer. The piece covers Tenstorrent's architecture in detail, frames the broader AI hardware startup competitive landscape, and provides a valuation perspective on Tenstorrent relative to ARM and Cerebras.

**Tenstorrent Architecture.** The Blackhole (gen 2) chip uses a mesh topology with 16 big RISC-V CPU cores for general-purpose computation and 725 baby RISC-V cores (under 1% of die area) for kernel launching and data movement. Tensix cores are the AI compute building blocks, each containing five baby RISC-V cores. The gen 3 chip (Grendel) moves to a chiplet architecture separating high-performance RISC-V CPU and AI cores, though it will be built on Samsung Foundry SF4X — a node worse than TSMC N5. The software stack is on its sixth major revision, now unified from high-level ML graph compilation (Buda) down to low-level kernels (Metalium, TT-NN, TT-MLIR), with an active open-source community contributing top-performing kernels.

**Architectural Philosophy.** Senior architect Davor Capalija argued that Tenstorrent's design is architecturally superior to Nvidia GPUs (which carry legacy graphics baggage and a bolted-on TMA), Google TPUs (large cores with utilization problems), and exotic ahead-of-time-compiled chips like Groq and Cerebras. The author broadly agrees with this framing but stresses that architectural correctness does not overcome CUDA's entrenched software moat. The author is explicitly skeptical of Groq's gross margin claims and considers Cerebras comically overvalued.

**AI Hardware Startup Framework.** Horizontal training hardware is described as a dead market — hyperscalers build semi-custom silicon (Google TPU, Amazon Trainium, Microsoft Maia) via Broadcom, Marvell, and similar design partners, while AMD provides cheap commodity alternatives and neoclouds offer depreciated H100s at collapsing rental prices. The only viable path for startups is inference, and only via extreme cost or performance differentiation. Tenstorrent's use of Samsung SF4X and DRAM (not HBM) enables a potential 60% gross margin while undercutting on price.

**Valuation.** Tenstorrent closed a Series D at $2B. The author values the RISC-V IP business alone at ~1% of ARM's market cap (~$1.6B), given ARM's aggressive royalty increases and SiFive's collapse as a high-performance RISC-V alternative. Tenstorrent is judged the only investment-grade AI hardware startup. SambaNova (CGRA architecture) and Positron AI (galaxy-brain founder) receive honorable mentions.

## Calls

- [[NVDA]] — LONG — px@$16 avg — Author's largest position; CUDA moat and dominant scale make it the default winner even against architecturally superior challengers.
- [[ARM]] — NEUTRAL — px@n/a — ARM's aggressive licensing behavior creates an opening for Tenstorrent's RISC-V IP; author's finance peers consider ARM's valuation stretched but stock has held.
- [[CBRS]] — SHORT — px@n/a — Cerebras judged comically overvalued relative to Tenstorrent; author explicitly plans to trade it (bearish) post-IPO.
