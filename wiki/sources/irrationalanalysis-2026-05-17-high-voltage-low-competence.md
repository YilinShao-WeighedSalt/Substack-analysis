---
type: source
title: "High Voltage, Low Competence"
tags: []
related: []
created: 2026-05-17
updated: 2026-05-17
authors: [irrationalanalysis]
year: 2026
url: "https://irrationalanalysis.substack.com/p/high-voltage-low-competence"
venue: Irrational Analysis
post_date: 2026-05-17
tickers: [WOLF, IFX, AIXA, NVTS, TXN, ON, GFS, ENPH, SEDG, LITE, AAOI, COHR, VRT, ETN]
---

[[irrationalanalysis]] argues that the SiC/GaN power semiconductor market is undergoing a fundamental regime shift — away from the EV-driven race-to-the-bottom (where Chinese manufacturers and over-builders like Wolfspeed dominated the narrative) toward a quality-based pricing regime driven by datacenter and grid infrastructure demand. The author conducted an extensive datasheet comparison across 650V GaN, 1200V SiC, and 1700–2000V SiC device classes, building intuition via LTSpice circuit simulations, to determine which vendors actually have the best discrete MOSFETs.

**Key technical findings:** For 650V GaN, TI and Navitas are clearly first place due to both superior FET performance and integrated gate driver/protection circuits that eliminate the painful negative gate drive complexity — Infineon is second, STM in development. For 1200V SiC, Infineon is the dominant winner with extraordinarily low Rds_on, capable of handling 800W dissipation with proper liquid cooling. For 1700–2000V SiC, Infineon again wins via its 2000V part; Navitas is second. Wolfspeed's 10KV SiC part is viewed as genuinely exciting and uniquely enabling for solid-state transformers (SST), despite severe temperature sensitivity on Rds_on requiring custom cooling.

**The SST thesis** is the post's most emphatic call: the author believes solid-state transformers represent a far larger and more margin-rich opportunity than inside-datacenter power conversion. AI datacenters create massively destabilizing transient loads for the grid (multi-megawatt swings during training all-reduces), and traditional transformers simply pass this noise downstream. SSTs add active load/voltage/phase regulation and reduce reactive power needs — a premium that is now justified by the datacenter catalyst. Delta Electronics is named as the key SST incumbent.

**Multi-sourcing limitations** reinforce the quality story: unlike EV designs where you can compensate with a bigger battery, datacenter and grid applications cannot accept lower-efficiency second-source parts. This structural shift means gross margin expansion for quality leaders.

**Enphase and SolarEdge surprise:** Despite the home solar market being "dead" post-tax-credit removal, the author finds their core competence — safety, control ASICs, and distributed systems engineering for high-voltage DC-to-AC conversion — to be underappreciated and potentially actionable.

## Calls

- [[WOLF]] — LONG — n/a — 10KV SiC part is uniquely positioned for the SST revolution; enables drastic simplification of grid-interfacing circuits despite over-building history
- [[IFX]] — LONG — n/a — dominant SiC 1200V leader with extraordinary Rds_on; author has $50K queued to deploy into IFX; makes own GaN wafers (no Innoscience risk)
- [[AIXA]] — LONG — n/a — near-monopoly in GaN epitaxy equipment; also dominant in InP; author calls it a 'STONK' and is actively buying
- [[NVTS]] — LONG — n/a — best-in-class GaN FET with integrated protection; cross-licensing and second-source agreement with Infineon; SiC division is weak
- [[TXN]] — MENTION — n/a — best GaN integration alongside Navitas but sold out due to non-pure-play status
- [[ON]] — NEUTRAL — n/a — sold out at 15% profit; lateral GaN and SiC are both mediocre; vertical GaN is speculative with no public datasheets
- [[GFS]] — LONG — n/a — makes GaN wafers for Navitas; benefits as Innoscience (Chinese competitor) faces headwinds
- [[ENPH]] — LONG — n/a — home solar corpse with underappreciated core competence in safety circuits and control ASICs; author finds the bear case weaker than expected
- [[SEDG]] — LONG — n/a — same core competence argument as Enphase; distributed high-voltage DC-to-AC inverter safety/control expertise is the real moat
- [[LITE]] — MENTION — n/a — cited as hyperscaler-preferred domestic transceiver vendor that hyperscalers are propping up over Chinese suppliers; same dynamic seen in power semis
- [[AAOI]] — MENTION — n/a — same domestic transceiver supply-chain context as LITE
- [[COHR]] — MENTION — n/a — same domestic transceiver supply-chain context as LITE
- [[VRT]] — MENTION — n/a — named as a diversified incumbent in the SST opportunity alongside Eaton
- [[ETN]] — MENTION — n/a — named as a diversified incumbent in the SST opportunity alongside Vertiv
