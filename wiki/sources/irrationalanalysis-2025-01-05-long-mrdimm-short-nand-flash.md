---
type: source
title: "Long MRDIMM, Short NAND Flash"
tags: []
related: []
created: 2025-01-05
updated: 2025-01-05
authors: [irrationalanalysis]
year: 2025
url: "https://irrationalanalysis.substack.com/p/long-mrdimm-short-nand-flash"
venue: Irrational Analysis
post_date: 2025-01-05
tickers: [RMBS, WDC, MU, ONTO, CAMT, LRCX]
---

[[irrationalanalysis]] frames this post as a long/short pair trade entry into a fintwit contest: long MRDIMM (via Rambus) against short NAND flash (via Western Digital).

## Long MRDIMM — Rambus (RMBS)

MRDIMMs are next-generation memory modules that split a single stick into two virtual channels, roughly doubling bandwidth. Gen1 runs at 2×4400 MT/s (8800 MT/s effective) versus standard DIMM at 6000–6400 MT/s; Gen2 targets 12800 MT/s. Intel's Granite Rapids is the first platform to support MRDIMM, and AMD is expected to follow after JEDEC ratification.

An MRDIMM requires five non-DRAM component types: PMIC, temperature sensor, SPD Hub, Memory Data Buffer (MDB), and the MRCD clock driver. Rambus manufactures all five, making it an unusually pure-play leveraged to the MRDIMM ramp. The MDB chips require high-speed (~6 GHz) multiplexers, and the MRCD chip must arbitrate two active ranks simultaneously under strict one-cycle latency constraints — both non-trivial analog/mixed-signal design challenges.

Rambus's strategic moves reinforce the thesis: it sold its PHY IP assets to Cadence ~one year prior, signaling a deliberate pivot away from licensing toward MRDIMM silicon. The residual IP/royalty business carries ~95% gross margins but is seen as flat-to-declining as the EDA duopoly (Synopsys, Cadence) bundles competing controller IP. The product (MRDIMM chip) business operates at ~63% gross margins but is poised to scale with Granite Rapids production ramp and a second leg when 12800 MT/s MRDIMM arrives in ~12–18 months. Management's investor materials prominently feature a 42% CAGR projection for the segment. The author holds a small long in RMBS.

## Short NAND Flash — Western Digital (WDC)

NAND flash is characterized as the "most degenerate" memory segment. The industry is in a downcycle driven by weak smartphone and PC demand. Enterprise SSD demand has peaked even as datacenter capex continues rising — a bearish divergence. Someone (possibly Samsung or YMTC) is aggressively dumping, as evidenced by Micron's recent earnings commentary. YMTC's rapid share gains add structural pressure.

Western Digital was chosen over Kioxia as the short vehicle because: (1) WDC had an investor presentation ("New Era of NAND," June 2024) declaring the layer-count race over, while competitors are targeting ~1,000 layers within two years — a credibility-destroying call; (2) WDC is attempting to spin off its NAND division from the more stable HDD business, adding execution risk and potential borrow complications. The author holds a small short in WDC.

Other tickers mentioned as context: ONTO and CAMT as better-risk-adjusted plays on HBM advanced packaging; MU as a high-risk/high-reward HBM manufacturer; LRCX and Tokyo Electron as neutral semicap majors with memory exposure.

## Bonus: Samsung DS-Memory

Samsung's device (DX/MX) division has reportedly shifted LPDDR5X volume to Micron because Samsung DS pricing was too high. DS-Memory cannot cut prices further due to poor product quality and share losses to CXMT. DS-LSI (Exynos) has failed to provide an alternative to Qualcomm's AP. The author reads this internal conflict as a sign Samsung Electronics is approaching a breaking point.

## Calls

- [[RMBS]] — LONG — n/a — Pure-play on MRDIMM ramp across all five non-DRAM component types; product revenue set to scale with Intel Granite Rapids and next-gen 12800 MT/s cycle.
- [[WDC]] — SHORT — n/a — NAND dumping cycle, self-inflicted credibility damage from premature 'layers race is over' call, pending NAND spin-off adds complexity.
- [[MU]] — MENTION — n/a — Flagged as high-risk/high-reward HBM manufacturer; NAND earnings commentary used to corroborate industry dumping.
- [[ONTO]] — MENTION — n/a — Cited as a better-balanced HBM advanced packaging exposure alongside CAMT.
- [[CAMT]] — MENTION — n/a — Cited as a better-balanced HBM advanced packaging exposure alongside ONTO.
- [[LRCX]] — MENTION — n/a — Semicap major with memory exposure; rated neutral by author.
