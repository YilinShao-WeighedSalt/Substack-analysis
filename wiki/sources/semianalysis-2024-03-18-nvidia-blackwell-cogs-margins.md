---
type: source
title: "Nvidia B100, B200, GB200 - COGS, Pricing, Margins, Ramp - Oberon, Umbriel, Miranda"
tags: []
related: []
created: 2024-03-18
updated: 2024-03-18
authors: [semianalysis]
year: 2024
url: "https://newsletter.semianalysis.com/p/nvidia-b100-b200-gb200-cogs-pricing"
venue: SemiAnalysis
post_date: 2024-03-18
tickers: [NVDA, MU, 000660.KS]
---
[[semianalysis]] (Dylan Patel, Myron Xie, and Chaolien Tseng) provides an early deep-dive into Nvidia's Blackwell GPU family — the B100 (codename Umbriel), B200, Miranda, and GB200 NVL platform (codename Oberon) — analyzing architecture, bill-of-materials, pricing strategy, and competitive moat.

**Architecture and packaging.** Blackwell stays on TSMC 4nm — no node shrink versus Hopper — and instead doubles silicon area, placing two reticle-limited compute dies on a single CoWoS-L substrate. CoWoS-L uses an organic RDL interposer with passive silicon bridges rather than a full active interposer; Blackwell is the first major high-volume product to adopt this approach, raising both per-package cost and yield complexity. Each GPU pairs with up to eight stacks of 8-hi HBM3E, reaching up to 192 GB of capacity. SK Hynix supplies the majority of HBM3E; Micron is a secondary supplier. Samsung has failed to qualify its HBM3E despite public claims, leaving it out of the Blackwell supply chain.

**Product segmentation.** The B100 (Umbriel) targets 700W and is designed for drop-in compatibility with existing H100/H200 server baseboards, minimizing customer infrastructure spend. The B200 raises TDP to 1,000W and requires a server redesign. Miranda, the standard next-generation SKU, adds PCIe Gen 6 and 800G-per-GPU networking and could receive a 288 GB HBM refresh — Nvidia has already secured all available supply of SK Hynix and Micron 36 GB HBM stacks for early-2025 ramp. The Oberon GB200 NVL platform is the product generating the most supply-chain excitement, combining multiple B200 dies in a liquid-cooled rack-scale system.

**Pricing power and margins.** The article frames Nvidia's pricing philosophy with the observation that "B stands for Benevolence," signaling that Blackwell pricing is surprisingly accessible relative to the performance uplift — a deliberate strategy to accelerate adoption while maintaining H100's already exceptional economics (gross margin exceeding 85%). Despite hyperscaler investment in competing silicon (AMD MI300X, Intel Gaudi 3, Google TPU, and various internal accelerators), Nvidia retains "supreme pricing power." The article asserts Blackwell "curb stomps" all competing accelerators with the sole exception of Google's TPU on certain workloads.

**Supply chain implications.** The move to CoWoS-L increases TSMC advanced packaging demand. HBM3E supply is highly concentrated, and Nvidia's forward purchasing of 36 GB stacks signals both supply security and potential scarcity for rivals. The combination of dual-die design and tighter HBM supply creates meaningful barriers to matching Blackwell's memory bandwidth and capacity in competing products.

**Competitive moat.** The analysis concludes that hyperscaler custom silicon development has not meaningfully eroded Nvidia's dominance in training and inference for frontier models. Nvidia's software ecosystem (CUDA), NVLink interconnect speeds (doubled versus Hopper), and supply-chain lock-in across CoWoS-L capacity and HBM3E allocation reinforce a durable pricing premium into 2025 and beyond.

## Calls

- [[NVDA]] — LONG — n/a — Blackwell sustains 85%+ gross margins with supreme pricing power; no competing accelerator closes the performance gap at scale
- [[MU]] — LONG — n/a — secondary HBM3E supplier to Nvidia Blackwell; benefits from Samsung's disqualification and Nvidia's aggressive HBM forward purchasing
- [[000660.KS]] — LONG — n/a — SK Hynix is the primary HBM3E supplier for Blackwell, holding majority share and supply locked up through early-2025 ramp
