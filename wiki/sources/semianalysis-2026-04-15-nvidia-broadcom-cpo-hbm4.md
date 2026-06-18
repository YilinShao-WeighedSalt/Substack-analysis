---
type: source
title: "ISSCC 2026: NVIDIA & Broadcom CPO, HBM4 & LPDDR6, TSMC Active LSI, Logic-Based SRAM, UCIe-S and More"
tags: []
related: []
created: 2026-04-15
updated: 2026-04-15
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/isscc-2026-nvidia-and-broadcom-cpo"
venue: SemiAnalysis
post_date: 2026-04-15
tickers: [NVDA, AVGO, MRVL, AMD, INTC, TSM, 005930.KS, 000660.KS, MSFT, 2454.TW]
---

[[semianalysis]] rounds up the major findings from ISSCC 2026, the last of three key semiconductor conferences alongside IEDM and VLSI. The authors highlight that this year's ISSCC was unusually market-relevant, with papers directly tied to AI accelerator trends across memory, optical networking, die-to-die interconnects, and processors.

**Memory:** Samsung presented its HBM4 architecture featuring 1c DRAM core dies on an SF4 logic base die, achieving 13 Gb/s per pin and 3.3 TB/s bandwidth — more than 2x the JEDEC HBM4 standard of 6.4 Gb/s. The SF4 base die lowers operating voltage by 32% vs. HBM3E but carries higher cost than SK Hynix's TSMC N12-based approach. Front-end 1c yields were ~50% in 2025, posing margin risk. SK Hynix disclosed 1c LPDDR6 at 14.4 Gb/s with an estimated bit density of 0.59 Gb/mm², and 1c GDDR7 at 48 Gb/s. Samsung's 4F² Cell-on-Peripheral DRAM (same as SK Hynix's Peri-Under-Cell) reduces core circuitry area from 17% to 2.7%, pointing toward hybrid-bonded DRAM later this decade. SanDisk/Kioxia BiCS10 NAND set a density record at 37.6 Gb/mm² with 332 layers. MediaTek's xBIT 10T SRAM bitcell achieves 22–63% higher density and 30%+ power reduction vs. standard 8T cells, addressing the stagnation of SRAM scaling across logic nodes.

**Optical Networking / CPO:** NVIDIA presented DWDM-based CPO using 32 Gb/s per lambda with 9 wavelengths for scale-up interconnects, complementing its COUPE 200G PAM4 optical engines for scale-out. The newly formed OCI MSA standardizes 200 Gb/s bi-directional links (4×50G NRZ per direction) for scale-up CPO, resolving prior confusion between NVIDIA's two CPO approaches. Broadcom demonstrated a 6.4T MZM optical engine (64 lanes × ~100G PAM4) tested in a Tomahawk 5 51.2T CPO system. Marvell showed an 800G coherent-lite transceiver at 3.72 pJ/b (half the power of full coherent), operating over 40km at under 300ns latency using O-band wavelengths.

**Die-to-Die Interconnects:** TSMC's Active LSI (aLSI) improves signal integrity over CoWoS-L by embedding active Edge-Triggered Transceiver circuits in the bridge die, achieving 32 Gb/s at 0.75V with only 0.36 pJ/b total power. Bump pitch tightens from 45 µm to 38.8 µm. The test vehicle appears to match AMD's MI450 GPU topology. Intel's UCIe-S implementation reaches 48 Gb/s/lane on 22nm, likely a prototype for Diamond Rapids Xeon.

**Processors:** AMD's MI355X doubles matrix throughput per compute unit (N3P, custom cells, denser placement) and cuts IO dies from 4 to 2, reducing interconnect power ~20%. Microsoft's Maia 200 pushes reticle-scale monolithic design to its limit on N3P with 10+ PFLOPs FP4, 6 HBM3E stacks, and 28×400Gb/s D2D links. Rebellions' Rebel100 AI accelerator uses Samsung SF4X + I-CubeS packaging — a potential proof point for Samsung's effort to win AI packaging share.

## Calls

- [[NVDA]] — LONG — n/a — CPO strategy clarified (DWDM scale-up + COUPE scale-out) and OCI MSA formation validates NVIDIA's optical roadmap
- [[AVGO]] — LONG — n/a — Tomahawk 5 CPO system demonstration confirms Broadcom's execution on co-packaged optics for hyperscale switching
- [[MRVL]] — MENTION — n/a — Coherent-lite 800G transceiver targets campus datacenter links; innovative but no explicit investment call
- [[AMD]] — MENTION — n/a — MI355X architectural deep-dive shows strong N3P execution; aLSI test vehicle suggests MI450 multi-die packaging design
- [[INTC]] — MENTION — n/a — UCIe-S and M3DProc hybrid bonding progress; Diamond Rapids packaging strategy outlined
- [[TSM]] — MENTION — n/a — Active LSI advances TSMC's packaging moat; increasingly indispensable for leading-edge AI accelerator packaging
- [[005930.KS]] — NEUTRAL — n/a — Samsung HBM4 achieves best-in-class pin speed but faces SF4 cost premium and ~50% 1c yield headwinds vs. SK Hynix
- [[000660.KS]] — MENTION — n/a — SK Hynix maintains HBM4 reliability/stability lead; 1c GDDR7 at 48 Gb/s extends density leadership
- [[MSFT]] — MENTION — n/a — Maia 200 details disclosed; reticle-scale monolithic approach validated for inference but trails multi-die peers in flexibility
- [[2454.TW]] — MENTION — n/a — MediaTek xBIT SRAM and Dimensity 9500 thermal innovations highlight design strength on TSMC N3
