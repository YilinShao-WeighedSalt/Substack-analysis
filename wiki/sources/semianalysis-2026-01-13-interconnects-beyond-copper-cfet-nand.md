---
type: source
title: "Interconnects Beyond Copper, 1,000 CFETs, SK Hynix Next-Gen NAND, 2D Materials, and More"
tags: []
related: []
created: 2026-01-13
updated: 2026-01-13
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/interconnects-beyond-copper-1000"
venue: SemiAnalysis
post_date: 2026-01-13
tickers: [000660.KS, 005930.KS, MU, LRCX, AMAT, 8035.T, TSM, 6670.T]
---

This IEDM 2025 round-up from [[semianalysis]] covers four major R&D themes shaping the next decade of chipmaking: 3D NAND scaling, post-copper interconnects, 2D transition metal dichalcogenide (TMD) transistors, and CFET progress.

**3D NAND.** SK Hynix (000660.KS) presented its 321-layer V9 NAND, adding a third deck to reach 21 Gb/mm² — a 44% density gain over the prior 238-layer generation. The authors note this density is only comparable to Micron's (MU) 276-layer G9 achieved with just two decks, implying Micron holds a structural cost advantage. Sandisk/Kioxia's (6670.T) upcoming 332-layer BiCS10 is expected to be far denser at 29 Gb/mm² TLC, further pressuring Hynix's competitive position. Samsung (005930.KS) is skipping 3xx-layer entirely, jumping from 286L V9 to 43x-layer V10 with three decks. Samsung also presented a molybdenum (Mo) wordline upgrade for V9, cutting contact resistance 40% and read time 30%, with Lam Research (LRCX) called out as dominating Mo ALD deposition tool share at the expense of AMAT (AMAT) tungsten tools. The high-aspect-ratio cryo etch needed for channel holes is another area where Lam traditionally leads, though TEL (8035.T) is encroaching. SK Hynix also showed a novel multi-site cell architecture enabling 5 bits-per-cell (5bpc) NAND by splitting each channel into two half-cylinders — a clever logical-scaling approach that is not yet cost-effective for production.

**Interconnects beyond copper.** Samsung demonstrated ruthenium (Ru) ALD with grain orientation engineering achieving 46% lower resistance vs. conventional processes in 300 nm² cross-sections, and 26% RC reduction in GAA FET simulations. IMEC published a roadmap showing the Cu-to-Ru transition starting at the A14-to-A10 node transition, with 16 nm pitch Ru metals (the limit of single-exposure High-NA EUV) targeted at A7. IMEC achieved >80% yield on two-layer Ru interconnects at 16 nm pitch using fully self-aligned vias.

**2D materials.** The section is a detailed assessment of MoS₂ and WSe₂ TMD FETs as silicon replacements below 10 nm gate lengths, where source-to-drain tunneling becomes critical. TSMC (TSM) showed p-type WSe₂ FETs with >100 cm²/V·s hole mobility using interlayer engineering, but p-type performance, variability, and lack of manufacturable doping remain first-order blockers. Wafer-scale integration, low-bias contact resistance, and TCAD modeling maturity are identified as prerequisites before 2D logic can matter commercially.

**CFET.** TSMC made unexpectedly strong progress (details paywalled) — teased as the most important paper at the conference.

## Calls

- [[000660.KS]] — MENTION — px@n/a — SK Hynix V9 NAND competitive position weaker than peers; Micron and Kioxia ahead on density-per-deck economics
- [[005930.KS]] — MENTION — px@n/a — Samsung Mo wordline upgrade improves V9 performance; skipping to 43x-layer V10 is an aggressive generational leap
- [[MU]] — MENTION — px@n/a — Micron 276L G9 achieves comparable density to Hynix 321L with only two decks, implying lower cost structure
- [[LRCX]] — LONG — px@n/a — Dominant in Mo ALD deposition tools (taking share from AMAT) and cryo etch for high-aspect-ratio NAND channels; WFE intensity rising with 3-deck NAND complexity
- [[AMAT]] — MENTION — px@n/a — Losing Mo deposition tool share to Lam as memory makers transition from tungsten to molybdenum wordlines
- [[8035.T]] — MENTION — px@n/a — TEL encroaching on Lam's cryo etch dominance for NAND high-aspect-ratio channel holes
- [[TSM]] — MENTION — px@n/a — TSMC showed unexpected CFET progress and credible p-type 2D FET results; positioned as leading-edge logic technology leader
- [[6670.T]] — MENTION — px@n/a — Sandisk/Kioxia BiCS10 332L expected at 29 Gb/mm² TLC, significantly denser than Hynix V9 and competitive pressure on Samsung
