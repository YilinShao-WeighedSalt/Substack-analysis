---
type: source
title: "NVLink Fusion: Jensen Murders UALink with Galaxy-Brain Strategy"
tags: []
related: []
created: 2025-05-22
updated: 2025-05-22
authors: [irrationalanalysis]
year: 2025
url: "https://irrationalanalysis.substack.com/p/nvlink-fusion-jensen-murders-ualink"
venue: Irrational Analysis
post_date: 2025-05-22
tickers: [NVDA, AVGO, AMD, SNPS, CDNS, MRVL, ALAB, QCOM, 3661.TW, 2454.TW]
---

Nvidia's announcement of NVLink Fusion is described as a galaxy-brain strategic move that reshapes the entire AI ASIC market. The core insight is that there are only two companies with high-quality 200 Gbps SerDes PHYs — Nvidia and Broadcom — and this announcement weaponizes that advantage.

The technical crux: NVLink C2C (short-range 200G SerDes) is now licensable as IP to third parties, but NVLink5 (long-range 200G SerDes) is deliberately withheld. Instead, Nvidia sells a "Fusion chiplet" that bridges NVLink C2C on one side to NVLink5 on the other. Critically, Nvidia controls which configurations are supported: (1) third-party ARM CPU + Nvidia GPU, or (2) Nvidia Grace CPU + third-party ASIC + NVLink Fusion chiplet. Any other combination — such as a third-party CPU plus a third-party ASIC together — is unsupported and deliberately kneecapped to single-node reach.

UALink, the AMD-donated open standard, is effectively killed. The spec requires an IEEE 802.3dj Ethernet PHY, and with neither Nvidia nor Broadcom participating, no high-quality 200G PHY exists for UALink. Volume ramp was already far out (likely 2027), and with Astera Labs defecting to NVLink Fusion, the switch ecosystem has collapsed.

Company-level impacts are granular. Synopsys and Cadence lose TAM in their IP divisions as Nvidia directly competes with a superior 200G PHY, though core EDA is unaffected. Alphawave is in severe trouble, potentially losing a rumored Qualcomm acquisition. Marvell openly admits its 200G SerDes is inadequate after failures on the Amazon Trainium 3 program. Alchip also struggled integrating Synopsys 200G and had to re-spin. Astera Labs joined NVLink Fusion, which shrinks its PCIe switch market and calls into question its heavy R&D spend on its own 200G SerDes. Google has desperately sought any viable 200G SerDes to design out Broadcom and failed; MediaTek reportedly failed twice and lost half its SerDes team to Nvidia. Broadcom is framed as a net beneficiary — competitors are eliminated, hardening a duopoly. Qualcomm and Fujitsu are positioned as winners for custom ARM CPU plays that slot into the NVLink Fusion ecosystem.

[[irrationalanalysis]] frames this as Nvidia protecting long-reach SerDes IP while flooding the ecosystem with short-reach C2C to lock in third-party designs — generating strategic moat, not direct revenue.

## Calls

- [[NVDA]] — LONG — n/a — NVLink Fusion locks ecosystem into Nvidia, murders UALink, and protects long-reach SerDes IP in a Nvidia-only chiplet.
- [[AVGO]] — LONG — n/a — Duopoly in 200G SerDes hardens as Nvidia eliminates shared competitors; Broadcom is net beneficiary.
- [[AMD]] — SHORT — n/a — UALink is dead on arrival; no viable switch ecosystem and no competitive 200G SerDes path.
- [[SNPS]] — MENTION — n/a — IP division TAM shrinks as Nvidia directly competes; core EDA unaffected but some job losses likely.
- [[CDNS]] — MENTION — n/a — Same IP division TAM compression as Synopsys; core EDA business insulated.
- [[MRVL]] — SHORT — n/a — 200G SerDes publicly admitted as inadequate; Trainium 3 IO die win is a consolation prize after Alchip failures.
- [[ALAB]] — SHORT — n/a — PCIe switch market shrinks post-NVLink Fusion; in-house 200G SerDes R&D now questionable after joining program.
- [[QCOM]] — LONG — n/a — Custom ARM CPU benefits from instant large-market access via NVLink Fusion partnership.
- [[3661.TW]] — SHORT — n/a — Alchip failed Synopsys 200G SerDes integration on Trainium 3, forced re-spin, losing ground to Marvell.
- [[2454.TW]] — SHORT — n/a — MediaTek SerDes failed twice (N4P and N3P), half the team reportedly defected to Nvidia, Google design-in lost.
