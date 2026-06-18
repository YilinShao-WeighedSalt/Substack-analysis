---
type: source
title: "Hot Chips 2025: Irrational Recap"
tags: []
related: []
created: 2025-09-13
updated: 2025-09-13
authors: [irrationalanalysis]
year: 2025
url: "https://irrationalanalysis.substack.com/p/hot-chips-2025-irrational-recap"
venue: Irrational Analysis
post_date: 2025-09-13
tickers: [MRVL, AVGO, ALAB, SMTC, INTC]
---

[[irrationalanalysis]] covers the Hot Chips 2025 conference with opinionated, engineering-driven analysis, grouping presentations by topic rather than quality tier.

**Networking.** Intel's Smart NIC shared zero performance data despite featuring an RDMA engine. AMD's Pensando-derived Pollara NIC is characterized as two years behind Nvidia ConnectX, with poor performance and thin margins as a semi-custom Broadcom design. Nvidia's ConnectX presentation immediately followed AMD's, with the contrast described as devastating — AMD engineers in the audience visibly shocked by real benchmark numbers. On switching, Broadcom's Tomahawk 5 Ultra demonstrated strong low-latency and collectives support, leading the author to argue UALink has no remaining latency advantage: a future 200G SerDes UALink switch will require AEC or on-PCB retimers, pushing its effective latency worse than Broadcom's SUE/UEC stack shipping by H2 2026.

**Marvell and the Trainium 3 drama.** Marvell's Hot Chips presentation showed technically impressive 500mV SRAM and strong D2D PHY results, but the earnings call days later was the real event. The author argues guidance numbers implicitly confirmed Marvell lost the Trainium 3 ASIC socket to Alchip, while CEO Matt Murphy repeatedly pivoted rather than confirming it. Trainium 4 is being dual-tracked (NVLink Fusion vs. UALink), with Alchip making the main die for both tracks and Astera Labs positioned for the UALink switch variant. The author shorted MRVL at $72, covered quickly, and continues to trade it as a short vehicle. The author sarcastically proposes Marvell convert its buyback into AVGO purchases instead.

**d-Matrix.** The startup's in-SRAM compute architecture is interesting but faces headwinds from upcoming HBM4 base-die designs. Their key claim: custom 3D DRAM stacked to 4 layers achieves 60% lower cost than HBM4, 90% less IO energy, and 100x bandwidth advantage, sufficient for medium-sized language model inference at high batch sizes. The author finds the claims credible and views the technology as genuinely competitive.

**Google Ironwood (TPU 6p/7).** The 4×4×4 electrical cube architecture uses OCS only for inter-cube connectivity. The SparseCore sits on a separate ring NoC node for functional offload. VLIW compute is used, with Google cited as the only company capable of making a VLIW compiler work at scale. The author firmly dismisses recurring Taiwan rumors of MediaTek winning future TPU sockets, arguing Broadcom's position is locked in. Semtech is noted as having been hurt by ACC rack architecture changes.

**Miscellaneous.** Intel's Clearwater Forest (18A) presenter defended the node's reality under pointed audience questioning. IBM Power11 features a universal SerDes-based memory interface with only 6–8 ns effective latency penalty. A novel 3D-printed copper coldplate (ECAM) process from Fabric8 is highlighted as expanding thermal design space significantly.

## Calls

- [[MRVL]] — SHORT — px@72 (shorted at $72, covered same session) — lost Trainium 3 to Alchip, management obfuscating guidance, poor competitive position in networking; fun short-trading vehicle
- [[AVGO]] — LONG — px@n/a — Tomahawk 5 Ultra dominant in switching, Google TPU locked in, UALink irrelevant; author sarcastically recommends Marvell buy AVGO shares instead of buybacks
- [[ALAB]] — MENTION — px@n/a — positioned as UALink switch supplier for Trainium 4; author references losing money trying to short it ("cockroach of semiconductors")
- [[SMTC]] — MENTION — px@n/a — negatively impacted by ACC rack architecture changes, copper cable density suggests Catalina volume far below expectations
- [[INTC]] — MENTION — px@n/a — Clearwater Forest/18A presented; 17% IPC uplift noted but L2 latency questioned; audience trolled presenter about 18A viability
