---
type: source
title: "Is SMIC N+3's Metal Pitch Smaller than Intel 18A's?"
tags: []
related: []
created: 2026-06-14
updated: 2026-06-14
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/steel-smic-n3-teardown"
venue: SemiAnalysis
post_date: 2026-06-14
tickers: [INTC, TSM, QCOM, AAPL, AMD]
---

[[semianalysis]] tears down SMIC's N+3 node — used in Huawei's Kirin 9030 Pro — and examines whether its headline 32.5 nm M0 metal pitch actually beats Intel 18A's 36 nm. The short answer: technically yes, but it is a cherry-picked metric that conceals a wider capability gap.

**Density and patterning mechanics.** SMIC N+3 achieves 113.4 MTr/mm² transistor density, roughly on par with TSMC N6 (107.7 MTr/mm²), but only by applying self-aligned quadruple patterning (SAQP) on M0 — far more complex than TSMC N6's double patterning (SADP). M1 pitch is 38 nm (using a 3:2 ratio to gate vs. N6's 1:1), M2 pitch is 40 nm, and cell height is 228 nm vs. 240 nm for TSMC N6. The smaller M0 pitch is a local intra-cell routing layer; M1–M3 pitches and track density matter far more for real design capability, where SMIC lags.

**Performance reality.** The Kirin 9030 Pro SoC performs similarly to three-year-old Android flagships and trails current leaders from Apple, Qualcomm, MediaTek, and Samsung by 2.7×. Apple's efficiency cores deliver 20% higher integer performance at just 1 W versus 4.5 W for Huawei's prime core; per-clock efficiency is 35% below Apple's 2020-era M1 Firestorm.

**Manufacturing complexity and cost.** Cascaded SAQP creates re-entrant M0 trenches and barrier-rich footing, raising mask count and yield risk. SRAM uses 8T cells rather than standard 6T, signaling stability challenges. Each future scaling step adds cost and process risk with no EUV available.

**Strategic implications.** Export controls are becoming less effective at the node level: SMIC has licensed N+2/N+3 to Hua Hong at government direction, and process knowledge is diffusing to Alibaba T-Head, Cambricon, and others. Huawei has developed domestic EDA to replace restricted Western tools. The LogicFolding roadmap targets 5 GHz frequencies by 2031 via 3D stacking. China's trajectory is sufficient for phones, inference, networking, and security-sensitive workloads — just not competitive with leading-edge EUV nodes for compute density.

**Bottom line.** SMIC N+3's smaller M0 pitch is real but misleading; the process achieves TSMC N6-class logic density through greater complexity, not superior capability. Intel 18A retains a meaningful architectural advantage, and TSMC's EUV-based nodes remain well ahead. The more important story is Chinese semiconductor ecosystem diffusion making entity-list sanctions on individual fabs increasingly insufficient.

## Calls

- [[INTC]] — NEUTRAL — px@n/a — Intel 18A retains a real architectural edge over SMIC N+3 despite the misleading headline pitch comparison
- [[TSM]] — NEUTRAL — px@n/a — TSMC N6 matched in density only via far greater SMIC process complexity; EUV lead intact
- [[QCOM]] — MENTION — px@n/a — cited as a current flagship SoC vendor whose chips outperform the Kirin 9030 Pro by 2.7×
- [[AAPL]] — MENTION — px@n/a — Apple efficiency cores benchmark 20% higher integer performance at 4.5× lower power vs. Huawei prime core
- [[AMD]] — MENTION — px@n/a — listed among companies whose process knowledge is part of the broader competitive context
