---
type: source
title: "Co-Packaged Optics (CPO) Book Scaling with Light for the Next Wave of Interconnect"
tags: []
related: []
created: 2026-01-01
updated: 2026-01-01
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/co-packaged-optics-cpo-book-scaling"
venue: SemiAnalysis
post_date: 2026-01-01
tickers: [NVDA, AVGO, MRVL, LITE]
---

[[semianalysis]] argues in this comprehensive deep-dive that co-packaged optics (CPO) offers limited near-term benefits for scale-out networking but represents the critical enabling technology for scale-up networking for the remainder of this decade — making CPO adoption a matter of "when and how, not if and why."

**Scale-out vs. scale-up distinction.** Scale-out networking accounts for 85% of cluster networking cost and 86% of networking power, yet CPO delivers only a 3% total cluster cost reduction and 2% total cluster power savings in a three-layer network — insufficient to overcome serviceability anxiety and bargaining-power concerns (single switch vendor vs. multiple transceiver suppliers). Scale-up networking, by contrast, is currently constrained to 2-meter copper reach; CPO unlocks significantly larger "world sizes" across racks and represents a far larger TAM.

**Power and cost economics.** CPO cuts individual 800G link power by 73% (16–17W DSP transceiver → 4–5W CPO system), confirmed by Meta's testing on Broadcom's Bailly 51.2T switch (15W → 5.4W, a 65% reduction). However, vendor margin stacking on optical engines erodes cost advantages: 36 optical engines at $1,000 manufacturing cost become $80–90k to end customers vs. $72k for equivalent transceivers. Two-layer network deployments fare better, achieving 48% networking power reduction and 4% total cluster power savings.

**Reliability data.** Meta's ECOC 2025 study of Broadcom's Bailly switch logged zero uncorrectable codeword failures across 15 million 400G port-device hours (~325 days), with CPO MTBF estimated at 2.6M device hours — roughly 5x better than pluggable 400G transceivers (550k hours). Key caveat: lab conditions differ materially from production datacenters.

**Manufacturing standard: TSMC COUPE.** TSMC's Compact Universal Photonic Engine (EIC on N7, PIC on SOI N65, bumpless SoIC bonding) is emerging as the industry standard. Nvidia exclusively adopts COUPE; Broadcom is transitioning away from SPIL FOWLP; Ayar Labs pivoted from Global Foundries monolithic to COUPE for its second-generation TeraPHY chiplet.

**Key company positions.** Nvidia's Quantum X800-Q3450 CPO switch offers 144×800G ports and its Spectrum-X Photonics (co-developed with Broadcom) offers 512×800G ports; Nvidia treats its scale-out CPO launch as a "pipe-cleaner" for the more critical scale-up application. Broadcom's Bailly 51.2T is already shipping in limited volumes. Marvell acquired Celestial AI (December 2024), a CPO specialist targeting Amazon Trainium 4, with an estimated $1B revenue run rate by end of 2028. Lumentum supplies single high-power DFBs to Nvidia's laser ecosystem.

**Adoption timeline.** 2025–2026: limited scale-out adoption, hyperscaler field testing. 2027–2028: scale-up CPO deployment inflects with Trainium 4 and similar custom AI chips. 2028+: CPO central to scale-up bandwidth scaling for the rest of the decade, with interposer-based integration potentially enabling 12.8 Tbps per optical engine.

## Calls

- [[NVDA]] — LONG — px@n/a — CPO is central to Nvidia's NVLink scale-up roadmap; Spectrum-X Photonics positions it across both scale-out and scale-up interconnect markets
- [[AVGO]] — LONG — px@n/a — Bailly 51.2T CPO switch shipping in volume with strong reliability data; co-developing Spectrum-X Photonics with Nvidia
- [[MRVL]] — LONG — px@n/a — Acquisition of Celestial AI positions Marvell for ~$1B CPO revenue run rate by end of 2028 via Amazon Trainium 4 scale-up integration
- [[LITE]] — MENTION — px@n/a — Named as Nvidia's laser supplier (single high-power DFBs) for CPO external light sources; component-level exposure to CPO ramp
