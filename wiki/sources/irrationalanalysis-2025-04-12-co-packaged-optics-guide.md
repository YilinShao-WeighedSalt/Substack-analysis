---
type: source
title: "A Background-Proof Guide on Co-Packaged Optics"
tags: []
related: []
created: 2025-04-12
updated: 2025-04-12
authors: [irrationalanalysis]
year: 2025
url: "https://irrationalanalysis.substack.com/p/a-background-proof-guide-on-co-packaged"
venue: Irrational Analysis
post_date: 2025-04-12
tickers: [MRVL, FN, TSM, GFS, TSEM, NVDA, AVGO, COHR, LITE, GLW]
---

[[irrationalanalysis]] delivers a technical deep-dive on co-packaged optics (CPO), arguing it is inevitable as electrical channels hit a hard wall at 448G SerDes. The post covers channel physics, light sources, photodetectors, and modulator topologies before turning to investment implications.

The core technical thesis: electrical channels suffer catastrophic frequency-selective fading and package-level crosstalk that "magic materials" cannot fix — optical channels, by contrast, offer terahertz of bandwidth at negligible loss per kilometer. The author debunks the "silicon beachfront" obsession, asserting that package crosstalk — not die I/O — is the binding constraint at 200G+.

On modulators, the post frames the industry debate as "Clan Micro-Ring vs. Clan Mach-Zehnder" and calls it a false choice. MRMs enable dense DWDM with minimal insertion loss but are thermally unstable; MZMs are stable but large and lossy in DWDM chains. Nvidia's Quantum-X uses MRMs with liquid cooling and chunky aluminum heatsinks to manage thermal variation; Broadcom's Hot Chips 2024 solution is suspected to use MZMs given the lack of bragging about rings. Both are deemed excellent. TSMC's COUPE hybrid bonding and CoWoS-L packaging are highlighted as decisive moats, achieving sub-3 dB insertion loss and strong crosstalk isolation — forcing PIC designs onto TSMC despite its weak photonics process node.

On investment calls: Marvell's Inphi-acquired oDSP business is the clearest loser — CPO eliminates the optical DSP entirely, and the author projects 50–70% revenue decline by 2030. Marvell's own CPO solution is characterized as vaporware after a confrontational OFC booth visit. Marvell is called an "attractive funding short." Fabrinet is the standout long: CPO's IP sensitivity and manufacturing complexity play directly to its cleanroom segregation model. Corning and Nittobo are flagged for optical fiber exposure. GlobalFoundries and Tower Semi face existential threat from TSMC's packaging lock-in policy despite having superior photonics process nodes. Laser manufacturers Lumentum and Coherent have transceiver revenue headwinds despite CPO logo appearances at GTC.

## Calls

- [[MRVL]] — SHORT — px@n/a — oDSP revenue from Inphi acquisition is structurally eliminated by CPO; CPO solution is vaporware; attractive funding short
- [[FN]] — LONG — px@n/a — uniquely positioned for CPO ramp due to IP segregation, trusted manufacturing partner status, and optical assembly expertise
- [[TSM]] — LONG — px@n/a — COUPE hybrid bonding and CoWoS-L packaging create a moat that forces PIC designs onto TSMC despite weak photonics process node
- [[GFS]] — SHORT — px@n/a — photonics node business threatened by TSMC packaging lock-in; shareholders warned
- [[TSEM]] — SHORT — px@n/a — photonics node business threatened by TSMC packaging lock-in; shareholders warned
- [[NVDA]] — MENTION — px@n/a — has a credible CPO solution (Quantum-X) using MRMs with liquid cooling and TSMC COUPE
- [[AVGO]] — MENTION — px@n/a — has a credible CPO solution (Hot Chips 2024) with strong TDEQ metrics, likely MZM-based
- [[COHR]] — MENTION — px@n/a — laser manufacturer with transceiver exposure; GTC logo appearance not sufficient reason to buy
- [[LITE]] — MENTION — px@n/a — laser manufacturer with transceiver exposure; GTC logo appearance not sufficient reason to buy
- [[GLW]] — MENTION — px@n/a — optical fiber exposure via communications segment; author considering foreign fiber exposure (Nittobo) as USD hedge
