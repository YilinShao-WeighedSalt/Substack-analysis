---
type: source
title: "Intel 18A Details & Cost, Future of DRAM 4F2 vs 3D, Backside Power Adoption (or Not), China's FlipFET, Digital Twins from Atoms to Fabs, and More"
tags: []
related: []
created: 2025-07-21
updated: 2025-07-21
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/vlsi2025"
venue: SemiAnalysis
post_date: 2025-07-21
tickers: [INTC, MU, LRCX, TSM, 000660.KS]
---

[[semianalysis]] covers the key process technology and memory architecture disclosures from VLSI 2025, spanning Intel 18A, DRAM scaling paths, backside power delivery, China's FlipFET transistor concept, digital twin tooling, and emerging 2D materials challenges.

**Intel 18A** made its most detailed public production disclosure at the conference. The node's SRAM bitcell lands at 0.0210 µm² — roughly on par with TSMC N5 and N3E — but sits approximately 30% less dense than TSMC N2. The shift from FinFET to gate-all-around accounts for the bulk of density gains over Intel 3. Backside power delivery is confirmed as production-ready on 18A, the first such implementation at scale, though adoption across the industry is described as non-universal and cost-dependent.

**DRAM scaling** occupies a large share of the analysis. SK Hynix presented the two core bottlenecks limiting continued 6F2 shrinks: shrinking cell contact open margins and rising cell external resistance as bitlines scale down. The 4F2 vertical-channel transistor architecture resolves both by burying the bitline and eliminating the U-shaped current path, but it introduces steep high-aspect-ratio etch/deposition requirements and demands EUV patterning. Peripheral circuit integration options — under-cell (requiring fusion bonding) or on-cell (requiring sub-50nm hybrid bonding) — remain undecided. Chinese chipmakers are flagged as potential disruptors via 3D DRAM paths that sidestep leading-edge lithography.

**Micron** disclosed updated NVDRAM (Non-Volatile DRAM) metrics: a ferroelectric HZO 4F2 cell scaled 27% to 41nm pitch, achieving nearly 0.6 Gb/mm² — surpassing commercial DRAM density. However, energy savings are estimated at roughly $1/year per DIMM, insufficient to justify exotic pricing on $300+ DIMMs. The underlying techniques (ruthenium wordlines, vertical-channel transistors, CMOS-under-array) are viewed as foundational for future standard DRAM nodes.

**China's FlipFET**, developed at Peking University, targets CFET-level PPA without monolithic integration complexity. The approach forms stacked fins/nanosheets, completes high-temperature epitaxy for the top device, flips the wafer for BEOL processing, then flips again for lower-temperature backside steps. Self-alignment simplifies threshold voltage tuning but introduces warpage and overlay error risks; integration on a single wafer remains unvalidated. CFET high-volume adoption is described as roughly a decade away.

**Digital twins** span three scales: atomic (GPU-accelerated DFT-NEGF achieving 9.3x speedup with 4x A100s vs CPU), wafer (Lam Research's SEMulator3D for virtual process window optimization), and fab-level (targeting lights-out fab operation by 2035–2040). TSMC is also developing eDRAM in BEOL metal layers, but at 63.7 Mb/mm² the macro density trails commercial DRAM by roughly 9x.

## Calls

- [[INTC]] — MENTION — px@n/a — Intel 18A confirmed with production-ready backside power delivery; SRAM density at parity with TSMC N3E but ~30% below N2, validating node competitiveness while acknowledging trailing-edge density gap
- [[MU]] — MENTION — px@n/a — NVDRAM demonstrates best-in-class 4F2 cell density (~0.6 Gb/mm²) and foundational techniques for future DRAM nodes; near-term economics of ferroelectric NV premium remain unattractive
- [[LRCX]] — MENTION — px@n/a — SEMulator3D digital twin software enables virtual plasma and etch process optimization, compressing physical recipe iterations for advanced patterning customers
- [[TSM]] — MENTION — px@n/a — TSMC N2 projected 22% scaling vs N3E primarily from non-bitcell periphery gains; eDRAM BEOL demo is early-stage R&D far below commercial density targets
- [[000660.KS]] — MENTION — px@n/a — SK Hynix presented the definitive technical case for 4F2 DRAM, identifying cell contact margin and external resistance as the critical blockers to continued 6F2 scaling
