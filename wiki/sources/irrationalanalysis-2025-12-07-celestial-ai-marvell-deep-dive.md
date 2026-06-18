---
type: source
title: "Celestial AI // Marvell Deep Dive"
tags: []
related: []
created: 2025-12-07
updated: 2025-12-07
authors: [irrationalanalysis]
year: 2025
url: "https://irrationalanalysis.substack.com/p/celestial-ai-marvell-deep-dive"
venue: Irrational Analysis
post_date: 2025-12-07
tickers: [MRVL, NVDA]
---

[[irrationalanalysis]] examines Marvell's acquisition of Celestial AI — a deal the author characterizes as having only two possible outcomes: a transformative win on par with the Mellanox and Inphi acquisitions combined, or a catastrophic zero.

**Background and deal structure.** The author previously dismissed Marvell as "co-packed optics losers" due to their DR-MZI light engine approach. The Celestial AI acquisition changes that view, as Marvell is discarding its prior silicon photonics direction entirely in favor of Celestial's germanium EAM (electro-absorption modulator) technology. The deal includes an earnout clause requiring Celestial to deliver a minimum of $500M in revenue in calendar year 2028, and Amazon received additional warrants at $87/share. The author reads the 2028 earnout date as an implicit admission that meaningful revenue in CY2026 or CY2027 is unlikely — consistent with GR-468 reliability qualification timelines.

**Ring modulators vs. germanium EAM.** Celestial's core pitch rests on attacking ring modulator technology as thermally unstable. The author validates this technically — rings are highly sensitive to thermal drift, which degrades extinction ratio (the optical 0/1 contrast) from ~15 dB down to ~4 dB when out of setpoint, making signal recovery unreliable. However, the author argues Celestial is simultaneously right about the problem and wrong about its unsolvability: Nvidia, in partnership with TSMC on the COUPE silicon photonics platform, has demonstrably solved ring modulator thermal control at scale, with high-volume ring-based transceivers and CPO switches ramping in 2026. Nvidia's ~18-month head start on COUPE represents a meaningful competitive advantage, and the earnout race means Celestial must prove out revenue by 2028, by which point Nvidia and others may have already captured the market.

**Germanium EAM reliability risk — the central bear case.** Celestial's tech stack revolves around Ge-EAM, acquired partly through Rockley Photonics' patent portfolio (purchased October 2024, ~2 years after Rockley's chapter 11 bankruptcy filing in January 2023). The key unresolved issue is GR-468 qualification: germanium EAM structures exhibit lattice mismatch, dark current degradation, SNR and extinction ratio drift, and different failure modes from standard germanium photodiodes found in ordinary SiPho. The 2028 earnout coincides precisely with how long full GR-468 reliability testing takes, making qualification the defining gating factor for Celestial delivering on its revenue target.

## Calls

- [[MRVL]] — NEUTRAL — px@n/a — binary outcome: Celestial AI either transforms MRVL (Inphi + Mellanox-level impact) or goes to zero on GR-468 qualification failure
- [[NVDA]] — LONG — px@n/a — solved ring modulator thermal control at scale on TSMC COUPE; ~18-month head start in CPO puts Nvidia well ahead of Celestial's 2028 earnout target
