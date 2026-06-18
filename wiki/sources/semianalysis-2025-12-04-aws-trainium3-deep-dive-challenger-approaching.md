---
type: source
title: "AWS Trainium3 Deep Dive | A Potential Challenger Approaching"
tags: []
related: []
created: 2025-12-04
updated: 2025-12-04
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/aws-trainium3-deep-dive-a-potential"
venue: SemiAnalysis
post_date: 2025-12-04
tickers: [AMZN, NVDA, ALAB, CRDO, AMD, TSM, MU]
---
[[semianalysis]] delivers a deep technical and commercial analysis of AWS Trainium3 (Trn3), arguing it represents a meaningful step toward challenging Nvidia's AI accelerator dominance — but stops short of predicting a regime change, concluding Nvidia will "stay King of the Jungle" if it maintains pace.

**Chip architecture.** Trn3 moves to TSMC N3P from N5, adds MXFP8/MXFP4 support (MXFP8 FLOPS doubled vs Trn2), and upgrades to HBM3E at 9.6 Gbps pin speeds — the highest observed on any HBM3E deployment — for 144 GB per chip and a 70% bandwidth increase. Scale-up bandwidth doubles to 1.2 TB/s per chip via PCIe Gen 6. BF16/FP32 performance is unchanged from Trn2, which the authors flag as a researcher adoption risk.

**Rack SKUs.** Two variants: Teton3 PDS (NL32x2, air-cooled, 32 chips per rack, expected majority of 2026 deployments) and Teton3 MAX (NL72x2, liquid-cooled, 144 chips across two racks, comparable to Nvidia's GB200 NVL72). The topology shifts from Trn2's 2D/3D torus to a switched all-to-all fabric with three switch generations planned across the Trn3 lifecycle, trading near-term hop count for faster time-to-market.

**Software strategy.** AWS is open-sourcing NKI (kernel language), cuBLAS/cuDNN/NCCL equivalents, and native PyTorch in Phase 1 — explicitly pursuing CUDA's ecosystem moat-building playbook. The critical gap: Logical NeuronCore (LNC=8) support is deferred to mid-2026, delaying broader research adoption. XLA/JAX stack is Phase 2.

**Supply chain and equity warrants.** Astera Labs (ALAB) supplies PCIe switches and retimers; AWS holds equity warrants translating to roughly a 23% effective discount. Credo (CRDO) supplies Active Electrical Cables with even larger warrant-based rebates — in some configurations, "Credo effectively paid Amazon to take AECs." HBM supply shifted from Samsung toward Hynix and Micron (MU) for better yield and speed. TSMC (TSM) manufactures Trn3 on N3P with CoWoS-R packaging.

**Competitive framing.** Authors characterize Nvidia (NVDA) as now fighting on three simultaneous fronts: Google TPUv7, AMD (AMD) MI450X with UALink, and AWS Trainium3. The piece warns Nvidia against the Intel-style complacency trap but sees no near-term displacement absent a slowdown in Nvidia's execution.

**Trainium4 roadmap.** Dual-track: UALink 224G and an Nvidia NVLink 448G BiDi chiplet fusion approach, with 8× HBM4 stacks (4× bandwidth, 2× capacity vs Trn3). Authors speculate AWS secured NVLink licensing well below Nvidia's typical ~75% gross margin, as Nvidia values ecosystem lock-in over per-deal economics.

## Calls

- [[AMZN]] — LONG — n/a — Trainium3 demonstrates credible perf/TCO execution across chip design, packaging, software, and supply chain, with warrant-based cost structures and dual-SKU deployment flexibility reducing time-to-monetization
- [[NVDA]] — LONG — n/a — Remains dominant AI accelerator vendor; three-front competitive pressure (Google, AMD, AWS) is a rising risk but authors conclude Nvidia stays king if execution pace holds
- [[ALAB]] — MENTION — n/a — AWS equity warrants provide ~23% effective discount on PCIe switches and retimers, making ALAB a preferred Trn3 switch supplier
- [[CRDO]] — MENTION — n/a — Warrant-based discounts on Active Electrical Cables so large that Credo effectively subsidized AWS adoption in some scenarios
- [[AMD]] — MENTION — n/a — MI450X with UALink cited as one of three competitive fronts threatening Nvidia's dominance
- [[TSM]] — MENTION — n/a — Manufactures Trn3 on N3P node with CoWoS-R packaging; Alchip and Annapurna handle package and front-end design respectively
- [[MU]] — MENTION — n/a — Mentioned alongside Hynix as preferred HBM supplier replacing Samsung for Trn3 due to better yield and pin-speed performance
