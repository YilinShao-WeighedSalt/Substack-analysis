---
type: source
title: "HBM: High-Bandwidth Mistake"
tags: []
related: []
created: 2026-05-31
updated: 2026-05-31
authors: [irrationalanalysis]
year: 2026
url: "https://irrationalanalysis.substack.com/p/hbm-high-bandwidth-mistake"
venue: Irrational Analysis
post_date: 2026-05-31
tickers: [005930.KS, MU, MRVL, ALAB, KORU]
---

[[irrationalanalysis]] presents a partial capitulation on DRAM as an investment, combined with a strong structural critique of HBM (High-Bandwidth Memory) as a long-term technology. The author argues HBM is fundamentally a mistake — the wrong solution to an I/O density problem — and will see a 90%+ volume drop within 7–10 years. In the near term, however, DRAM stocks likely have another double or triple ahead, followed by a 70%+ drawdown from peak at some point in the 3–10 year horizon.

**Engineering thesis:** DRAM has only four core attributes — latency, bandwidth, capacity, and power. HBM increases bandwidth via vertical stacking (TSVs and micro-bumps) but introduces parasitic bump capacitance that limits pin speeds and kills signal integrity. The HBM4 rollout at 11 Gbps/pin (vs. JEDEC's 8 Gbps spec) was an industry-wide fiasco: SK Hynix required ~6 re-spins on TSMC N12, Micron failed using an internal DRAM process for the base die, and even Samsung struggled. The author's view is that 11 Gbps is still poor compared to 32–64G SerDes already ubiquitous in logic. Custom HBM base dies (e.g., Marvell's) partially help but the TSVs remain the true bottleneck.

**Optimal long-term solution:** Clock-forwarded SerDes driving co-packaged optics (CPO), disaggregating LPDDR memory pools over optical links. Nvidia showed this direction at ISSCC 2026. This approach eliminates CDR/FEC overhead, achieves sub-3 pJ/bit, and enables memory reuse/reallocation across chips. The author estimates Nvidia is 2–3 years from scaling this; Broadcom and Marvell 3–5 years. Startup Positron is called out as the only AI ASIC company to have properly solved the memory bandwidth problem today, using only commodity LPDDR5X with no HBM.

**DRAM demand catalyst:** Agentic AI is a permanent, non-pull-forward structural demand driver. A Coatue video (Nick Gagnet, May 11 2026) projecting 5x memory demand in 5 years reinforced the author's view change. If HBM is eventually replaced by LPDDR at 3x supply, DRAM makers would see ~2.25x profits on 3x revenue at lower margins — a win-win for makers and customers.

**Stock pitch — Samsung (005930.KS):** Author's preferred DRAM play over MU and SK Hynix. Samsung has an in-house logic foundry (SF4X, ~TSMC N7/N6 PPA), deep experience in interface IP and logic design, and an internal silicon photonics process with a CPO design group. Co-design across HBM PHY, TSV PHY, and optical I/O gives Samsung a structural long-term advantage. Author is considering a ~$100K entry (via IBKR direct or KORU 3x levered Korea ETF). Micron is penalized for the base-die blunder and lack of high-speed signal integrity experience; SK Hynix will also suffer margin pressure from TSMC N3 base die costs.

**CXL** is noted as a partial solution (good for Marvell and Astera Labs) but insufficient — it layers a protocol on a sub-optimal PCIe PHY and does not fix the root I/O problem.

## Calls

- [[005930.KS]] — LONG — n/a — Samsung is the preferred DRAM play; in-house logic foundry, silicon photonics CPO, and co-design advantages make it structurally superior to Micron and SK Hynix
- [[MU]] — LONG — n/a — DRAM broadly has another double/triple ahead on agentic AI demand, but Micron is disadvantaged vs Samsung on HBM4 execution and lacks high-speed signal integrity expertise; author has no current position
- [[MRVL]] — MENTION — n/a — Custom HBM base die work and CXL position cited as partial solutions to the memory bandwidth problem
- [[ALAB]] — MENTION — n/a — Named alongside Marvell as a CXL beneficiary
- [[KORU]] — MENTION — n/a — Mentioned as a vehicle for leveraged Korean equity exposure to the Samsung DRAM thesis
