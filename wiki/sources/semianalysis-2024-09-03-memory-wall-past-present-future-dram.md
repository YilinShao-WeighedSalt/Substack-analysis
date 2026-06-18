---
type: source
title: "The Memory Wall: Past, Present, and Future of DRAM"
tags: []
related: []
created: 2024-09-03
updated: 2024-09-03
authors: [semianalysis]
year: 2024
url: "https://newsletter.semianalysis.com/p/the-memory-wall"
venue: SemiAnalysis
post_date: 2024-09-03
tickers: [MU, 000660.KS, 005930.KS, NVDA, 8035.T]
---

[[semianalysis]] argues that Moore's Law for DRAM effectively died a decade ago, with bit density increasing only 2x over the past ten years versus the historical 100x per decade. This stagnation has created a structural "memory wall" where compute improvements, though slowing, are vastly outpacing memory scaling — and AI is making the imbalance worse.

**The HBM Cost Crisis.** High Bandwidth Memory (HBM), the backbone of AI accelerator memory, costs 3x or more per GB than standard DDR5. For NVIDIA's H100, over 50% of manufacturing cost is attributed to HBM; for Blackwell, this rises to over 60%. HBM's expense stems from TSV-based die stacking (8–12 dies per stack, 1,200+ signal vias), strict binning requirements, and low packaging yields. SK Hynix leads in HBM3E yield via its MR-MUF packaging, while Samsung suffers from design mishaps and use of a trailing 1α node. Micron has a viable product but needs significant production scale-up.

**Why DRAM Stopped Scaling.** The core 1T1C cell architecture is unchanged since the 1970s. Capacitors now have 100:1 aspect ratios (~1,000nm tall, 10s of nm wide), with deposition and patterning at the limits of modern processing. Sense amplifiers face simultaneous pressure from shrinking area and smaller capacitor charge, making them increasingly sensitive to variation. Even EUV adoption in Samsung's 1z and SK Hynix's 1a nodes did not materially increase density.

**Near-Term Path: 4F² and Vertical Channel Transistors.** The theoretical density limit for a single-bit cell is 4F² (versus today's 6F²), offering a ~30% area reduction without shrinking minimum feature size. Vertical channel transistors (VCT) are required to achieve this layout. Chinese vendor CXMT already demonstrated 4F²/VCT in its 18nm DRAM at IEDM 2023, ahead of the major players, suggesting CXMT is struggling to scale minimum features. EVG and TEL (8035.T) stand to benefit from incremental wafer-bonding tool demand in VCT production.

**HBM4 and the Base Die Shift.** HBM4 targets up to 1.5 TB/s per stack at 16-Hi stacking and doubles bus width to 2048 bits. Critically, the base die will move to FinFET processes; SK Hynix has announced TSMC as its foundry partner. Custom base dies will allow offloaded DRAM state-machine control, daisy-chaining of HBM stacks, and modernized PHY interfaces. Eliyan (private), backed by Micron and Intel, is developing a custom UMI/Nulink standard to further improve interface bandwidth and energy per bit.

**Compute-in-Memory (CIM).** Current DRAM is massively bandwidth-constrained by its interface: the underlying bank potential is ~4 TB/s per 16 Gb chip, but HBM's external interface delivers only ~256 GB/s per die (1/16th of potential). Over 95% of HBM energy is consumed in the interface, not the memory cell. CIM aims to bring control logic on-chip, and the HBM4 custom base die creates a practical path for this.

**Emerging Alternatives.** FeRAM (ferroelectric RAM) showed competitive density at IEDM 2023 (Micron), but remains too expensive for volume production. MRAM (SK Hynix + Kioxia collaboration) reached 0.49 Gb/mm² density — slightly above Micron's D1β DRAM — but commercial products remain in the MB range. 3D DRAM is positioned as the longer-term architectural revolution, with major implications for wafer fab equipment vendors.

## Calls

- [[MU]] — LONG — n/a — Micron has viable HBM3E and leads in FeRAM R&D; needs production scale-up to compete with SK Hynix, but positioned for multi-year HBM demand tailwind
- [[000660.KS]] — LONG — n/a — SK Hynix is the clear HBM3E yield leader via MR-MUF packaging, capturing outsized margins as sole reliable supplier to NVIDIA for now
- [[005930.KS]] — MENTION — n/a — Samsung is losing HBM share due to yield issues and trailing node choice; recovery depends on resolving packaging deficiencies
- [[NVDA]] — MENTION — n/a — NVIDIA GPU bills of materials increasingly dominated by HBM cost (60%+ for Blackwell), creating margin sensitivity to memory pricing
- [[8035.T]] — MENTION — n/a — Tokyo Electron stands to gain from incremental wafer bonding tool demand as 4F²/VCT and HBM4 stacking complexity increases
