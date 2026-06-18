---
type: source
title: "Tower Semi, Fabrinet, and the Incredible Nvidia 1.6T Transceiver Ramp"
tags: []
related: []
created: 2025-08-22
updated: 2025-08-22
authors: [irrationalanalysis]
year: 2025
url: "https://irrationalanalysis.substack.com/p/tower-semi-fabrinet-and-the-incredible"
venue: Irrational Analysis
post_date: 2025-08-22
tickers: [TSEM, FN, COHR, MRVL, LITE, SITM, AAOI]
---

[[irrationalanalysis]] argues that the transition from 800G to 1.6T transceivers (200G per lane) is a decisive architectural inflection point, and that Nvidia has developed a ring-modulator-based Silicon Photonics (SiPho) EML architecture that structurally advantages Tower Semi and Fabrinet while severely disadvantaging Coherent and Marvell.

The post opens with a primer on transceiver laser architectures. VCSEL-based designs dominated up to 100G per lane but face serious reliability issues at 200G. The two EML alternatives are: (1) SiPho EML with a discrete SiPho PIC (typically sourced from Tower Semi) paired with external InP DFB lasers, and (2) monolithic InP EML, where the laser and modulator are on the same InP chip. SiPho EML suffers from alignment complexity and high laser power requirements; monolithic InP EML (Coherent's approach) suffers from poor yield on small InP wafers with large die sizes.

The core thesis derives from reading Tower Semi's and Fabrinet's earnings call transcripts together. Tower's CEO referenced ring add/drop filters on the receiver side, which the author interprets with near-certainty as Nvidia porting its ring-modulator design from TSMC SiPho to Tower SiPho. Fabrinet's stock fell on component shortage affecting its largest customer (Nvidia); the author identifies the shortage as Tower Semi SiPho PICs, not InP — consistent with the ring architecture requiring far less InP content than competing MZI EML designs.

Nvidia's ring architecture is argued to require roughly 1/4 to 1/2 the InP/DFB laser content of standard MZI EML, enabling Nvidia to price 1.6T transceivers at 50–70% gross margins while still undercutting Coherent. Coherent's monolithic InP MZI approach is doubly disadvantaged: large InP die with poor yield, and MZI modulator consuming far more wafer area than rings. Marvell is negatively impacted because ring modulators require different (higher) voltage swing and highly nonlinear PAM4 response, making a custom DSP (Nvidia's own) mandatory — gearboxing from 8×200G PAM4 to 16×100G NRZ is essential, cutting Marvell's DSP content. SiTime receives a mild positive as PPM clock sync is a natural fit for ring modulator systems. Lumentum is neutral-to-mild positive: it may lose module revenue to Nvidia but gains high-margin DFB laser sales.

## Calls

- [[TSEM]] — LONG — n/a — Nvidia ported ring-modulator SiPho design to Tower; SiPho PIC is the bottleneck component driving Fabrinet's shortage
- [[FN]] — LONG — n/a — Fabrinet assembles Nvidia's 1.6T transceivers; component shortage (Tower SiPho) is transient, volume ramp to follow
- [[COHR]] — SHORT — n/a — Monolithic InP MZI architecture has poor yield, cost disadvantage to Chinese rivals, and Nvidia ring pricing further compresses margins
- [[MRVL]] — SHORT — n/a — Ring modulators require custom DSP incompatible with Marvell's standard gearbox; Nvidia using internal DSP cuts Marvell out
- [[LITE]] — NEUTRAL — n/a — Loses some module business to Nvidia but gains high-margin DFB laser sales; net roughly neutral or modest positive
- [[SITM]] — LONG — n/a — Mild positive; PPM sync is a natural fit for ring-based transceiver architectures
- [[AAOI]] — MENTION — n/a — Noted as irrelevant to the ring architecture thesis; in its own separate situation
