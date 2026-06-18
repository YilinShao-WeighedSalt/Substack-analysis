---
type: source
title: "TSMC N2 + Next-Gen SoIC, Intel EMIB-T, Meta 3D Stacked Memory, CFET, 2D Materials, and More"
tags: []
related: []
created: 2025-02-05
updated: 2025-02-05
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/iedm2024"
venue: SemiAnalysis
post_date: 2025-02-05
tickers: [TSM, INTC, NVDA, AMAT, AMD, MU, META]
---

[[semianalysis]] published this IEDM 2024 round-up (authored by Jeff Koch and Dylan Patel) covering the key semiconductor device and packaging advances presented at the conference. The central thesis is that while the industry continues compounding incremental progress, the pace of device innovation is insufficient to keep up with exponential AI compute demand — a panel of experts closed the conference with a call for true breakthroughs, particularly in energy efficiency.

**TSMC N2** emerged as the clear leader in logic. The first GAA process node delivers 15% speed or 30% power improvement with >1.15x density scaling. Notable process innovations include barrier-less tungsten gate contacts (yielding a 55% RC reduction vs. a claimed 40% by AMAT) and an optimized M1 EUV patterning scheme that saves multiple masks and cuts M1 capacitance by 50%. Intel, Samsung, and Rapidus conspicuously did not present competing 2nm GAA papers, suggesting those nodes lack maturity. TSMC also led in **CFET** development, demonstrating a working inverter on real silicon — ahead of IMEC (simulation only) and Samsung/IBM's "stepped" approach that trades integration complexity for scaling penalties.

**Advanced packaging** received outsized attention. TSMC previewed next-gen **SoIC** 3D hybrid bonding at <15 µm TSV pitch, significantly tighter than Intel Foveros (~25 µm). Intel informally announced **EMIB-T**, adding TSVs to its existing embedded-bridge 2.5D technology to enable more flexible routing in complex heterogeneous HPC packages. **Nvidia** presented on defect-density scaling across the supply chain, noting defect rates below one per trillion vias — a systems-level supply chain achievement.

**Memory** discussions focused on compute-in-memory (CIM) as a longer-term solution to the AI memory wall, since HBM details remain too commercially sensitive to publish. SK Hynix showed an "AiM" (Accelerator in Memory) GDDR6 architecture with memory bandwidth per GB two orders of magnitude above HBM. **Meta** presented 3D stacked SRAM/DRAM atop compute, claiming 40% latency/energy reduction — though commercialization faces thermal budget incompatibilities and cost challenges. **AMD**'s X3D CPUs were cited as the only shipping hybrid-bonded memory-on-logic product. **Micron**'s NVDRAM was notably absent after debuting at IEDM 2023, suggesting the technology has not progressed toward productization.

**2D materials** (MoS₂ / WSe₂ channels) remain far from commercial readiness. TSMC showed contact formation for P-type devices and a full 2D FET inverter, while Intel demonstrated high-quality gate oxides. However, Samsung's on-wafer growth at 8" requires physical "clips" to hold films down — unscalable. Intel's 6nm gate length silicon GAA result likely pushes 2D materials further out on roadmaps by proving silicon can scale below the previously assumed 10nm limit.

Export control context: CXMT was absent from IEDM after the January 2025 rules extended coverage to their 18.5nm DRAM process; Chinese participation was skewed toward academics.

## Calls

- [[TSM]] — LONG — n/a — Apex predator of advanced logic; leads on N2, CFET, and SoIC across every dimension vs. peers
- [[INTC]] — MENTION — n/a — EMIB-T advances 2.5D packaging and 6nm gate length result is notable R&D, but absence on CFET and competing GAA nodes signals process maturity gaps
- [[NVDA]] — MENTION — n/a — Presented supply-chain defect-density excellence; no explicit financial stance but positioned as end beneficiary of packaging and process advances
- [[AMAT]] — MENTION — n/a — Barrier-less tungsten gate contact process referenced as TSMC N2 enabler; TSMC achieved 55% RC reduction vs. AMAT's claimed 40%
- [[AMD]] — MENTION — n/a — X3D CPUs cited as sole shipping hybrid-bonded memory-on-logic product, referenced in context of CIM cost challenges
- [[MU]] — MENTION — n/a — NVDRAM absent from IEDM 2024 after 2023 debut; suggests technology has not progressed to productization
- [[META]] — MENTION — n/a — Presented 3D stacked memory research for VR; promising energy efficiency gains but faces significant commercialization hurdles
