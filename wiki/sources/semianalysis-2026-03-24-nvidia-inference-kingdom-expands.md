---
type: source
title: "Nvidia - The Inference Kingdom Expands"
tags: []
related: []
created: 2026-03-24
updated: 2026-03-24
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/nvidia-the-inference-kingdom-expands"
venue: SemiAnalysis
post_date: 2026-03-24
tickers: [NVDA, INTC, 000660.KS, 005930.KS]
---

[[semianalysis]] delivers a deep technical and strategic analysis of Nvidia's GTC 2026 announcements, arguing that the company is systematically extending its dominance across inference infrastructure through a combination of novel chip disaggregation, standardized rack architectures, and strategic IP acquisition.

**Groq acquisition and LPU integration** is the centerpiece. Nvidia structured a $20B IP licensing deal with Groq — deliberately avoiding a formal acquisition to sidestep regulatory scrutiny — and is integrating Groq's LP30 LPU (third-generation, 500MB on-chip SRAM, 1.2 PFLOPs FP8) into its inference stack. The LP30 is manufactured on Samsung Foundry's SF4X node, chosen partly because it avoids TSMC allocation pressure. The LP40 roadmap migrates to TSMC N3P with CoWoS-R packaging and hybrid-bonded DRAM (supplied by SK Hynix).

**Attention FFN Disaggregation (AFD)** is the key algorithmic innovation: GPUs handle attention layers (memory-intensive, dynamic) while LPUs process feed-forward networks (stateless, deterministic). A ping-pong pipeline parallelism scheme hides GPU-LPU communication latency through All-to-All collective operations, maximizing KV cache capacity on GPU while leveraging LPU decode latency advantages.

**LPX rack architecture** fields 32 compute trays per rack with 16 LPUs each, 640TB/s aggregate scale-up bandwidth, and Altera (Intel) FPGAs as "Fabric Expansion Logic" for protocol conversion. Kyber racks densify to 4 GPUs + 2 Vera CPUs per blade (144 GPUs per rack), connected via NVLink 7 switches at 28.8Tbit/s per chip. The Vera ETL256 standalone CPU rack achieves 256 processors via extreme liquid-cooled density with Spectrum-6-based switch trays.

**Copper-first, optics-when-necessary** is Nvidia's explicit networking philosophy: all-copper scale-up within racks, CPO only for inter-rack connections. For Rubin NVL576 (8× Oberon racks), CPO connects inter-rack. For Feynman NVL1152, copper stays within racks and CPO bridges between racks. The article notes that 448G SerDes capabilities are insufficient for some connections, necessitating the CPO transition on that timeline rather than sooner.

**CMX/STX storage integration** adds a "Tier G3.5" NVMe layer for KV cache offloading in long-context inference, standardizing storage deployment with a reference architecture (1 Vera CPU + 2 CX-9 NICs + 2 SOCAMM modules per 1U box). A broad ecosystem of storage vendors — including Dell, HPE, IBM, NetApp, Supermicro, and VAST Data — has committed support.

The overall thesis is that Nvidia is constructing a vertically integrated inference kingdom: proprietary chips (GPU + LPU), proprietary interconnects (NVLink 7, NVSwitch), standardized rack form factors (Kyber, LPX, Vera, STX), and a software stack that ties them together — raising the cost of switching and widening the moat against disaggregated alternatives.

## Calls

- [[NVDA]] — LONG — px@n/a — expanding inference dominance via GPU+LPU disaggregation, standardized rack architecture, and copper-first networking moat
- [[INTC]] — MENTION — px@n/a — Altera FPGAs serve as Fabric Expansion Logic in LPX rack; Granite Rapids CPU referenced in system designs
- [[000660.KS]] — MENTION — px@n/a — SK Hynix supplies hybrid-bonded DRAM for LP40 roadmap; key beneficiary of Nvidia's advanced memory integration
- [[005930.KS]] — MENTION — px@n/a — Samsung Foundry manufactures LP30 on SF4X node; chosen partly due to favorable terms amid struggle to attract advanced AI logic customers
