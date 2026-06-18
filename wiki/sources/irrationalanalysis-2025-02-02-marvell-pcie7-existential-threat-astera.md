---
type: source
title: "Marvell PCIe 7 Switch: Existential Threat to Astera Labs"
tags: []
related: []
created: 2025-02-02
updated: 2025-02-02
authors: [irrationalanalysis]
year: 2025
url: "https://irrationalanalysis.substack.com/p/marvell-pcie-7-switch-existential"
venue: Irrational Analysis
post_date: 2025-02-02
tickers: [MRVL, ALAB, AVGO]
---

[[irrationalanalysis]] argues that Marvell is deep into development of a PCIe 7 switch product that poses an existential threat to Astera Labs' core AI-infrastructure franchise. The author's conviction stems from hands-on observation at DesignCon 2025, where two Marvell TSMC N3 SerDes demos stood out: one achieved 43 dB insertion loss at 1.6e-10 pre-FEC BER with no active cooling, and a second hit 45 dB at 1.7e-8 BER — both dramatically beating the PCIe 7 spec of 1e-6 pre-FEC BER at 36 dB. The PCB layout showed Rx traces removed (consistent with stressing Tx crosstalk, a known switch bottleneck) and the demo GUI referenced an "FPGA version" despite no discrete FPGA on board, implying integrated FPGA logic used to trial switching digital logic. The author concludes this is an old trial run of a PCIe switch and that a full PCIe 7 switch is already sampling privately.

On market structure, the post explains that PCIe switches were long an AVGO near-monopoly. Astera Labs carved out a niche (Scorpio-P) by offering a half-price product with exactly the lane count needed for AI head nodes, helped by Amazon warrant arrangements that incentivized AWS volumes. However: (1) Amazon has already shifted retimer sockets from Astera to Marvell under a new Marvell warrant agreement; (2) Astera licenses third-party SerDes, requiring retimers on every port and raising BOM costs, while Marvell owns its own superior SerDes; (3) with Amazon's Astera warrant conditions likely already met, AWS has no incremental incentive to keep buying Astera chips. The author contends sell-side models treating the PCIe switch market as majority-Astera are "incredibly wrong" and that Marvell will take the switch socket next.

The piece closes with a colorful call-out of investor Gavin Baker — a prominent ALAB bull — urging the finance community to alert him to Marvell's competitive move, which the author believes has gone unnoticed by consensus.

## Calls

- [[MRVL]] — LONG — px@n/a — Superior in-house SerDes and new AWS warrant position make it the likely winner of the AI PCIe switch socket.
- [[ALAB]] — SHORT — px@n/a — At risk of losing both retimer and PCIe switch sockets to Marvell as Amazon warrant incentives shift and SerDes quality gap widens.
- [[AVGO]] — MENTION — px@n/a — Historical PCIe switch near-monopoly; cited as context but seen as distracted by semi-custom silicon and not the primary competitive threat to Astera.
