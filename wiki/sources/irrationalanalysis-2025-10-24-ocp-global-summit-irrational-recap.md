---
type: source
title: "OCP Global Summit 2025: Irrational Recap"
tags: []
related: []
created: 2025-10-24
updated: 2025-10-24
authors: [irrationalanalysis]
year: 2025
url: "https://irrationalanalysis.substack.com/p/ocp-global-summit-2025-irrational"
venue: Irrational Analysis
post_date: 2025-10-24
tickers: [AVGO, MRVL, CRDO, ALAB, BE, PSTG, CIEN, TSEM, AMD, NVDA, FN, 002281.SZ, COHR]
---

[[irrationalanalysis]] covers the OCP Global Summit 2025 with a deep technical and investment-oriented recap, organized around four major themes: co-packaged optics (CPO), 400G electrical SerDes, optical transceivers, and scale-up protocols.

**Co-Packaged Optics (CPO):** The dominant theme at the show with 10+ dedicated talks. Broadcom (AVGO) was the standout — demonstrating zero failures in 1 million device hours of CPO field data, yielding a statistically-best MTBF claim of 2.5 million hours. The author argues forcefully that CPO is intrinsically more reliable than pluggable transceivers, citing elimination of wirebonds, fully integrated germanium PDs with wafer-level testing, and pluggable external lasers (ELSFP) that isolate the least reliable component. Accelink (002281.SZ) showed impressive ELSFP power stability. Marvell (MRVL) showed zero performance data — only block diagrams — which the author found disappointing despite viewing the CPO platform itself as promising. Ciena's Nubis acquisition presented a DWDM approach the author strongly disagrees with, preferring D2D clock-forwarded SerDes for density and efficiency.

**400G Electrical SerDes:** The author argues PAM4 400G SerDes is impractical for real channels (not just idealized MATLAB models), noting that crosstalk and high-frequency channel loss make standardization risky outside niche co-packaged copper channels. Ciena showed strong SerDes data but with a noise floor artifact suggesting ADC interleave calibration issues.

**Optical Transceivers:** Transceivers aren't going away, and the 800G cycle is at full ramp — Marvell will grow massively from this generation even if they lose share at 1.6T to Broadcom. Three conference sources claimed Marvell is out of Nvidia's 1.6T transceiver DSP in favor of Broadcom, but the author is skeptical this matters. Credo (CRDO) showed a 1.6T optical DSP with good pre-FEC BER and decent TDECQ results (using a lab-grade laser). Marvell's Alaska AEC demonstrated FEC symbol 4 at 7 meters — the author argued this is superior to Credo's product on reach, performance, latency, and power, and Marvell should compete more aggressively.

**Scale-Up Protocols / ESUN / UALink Death:** ALAB stock dropped on OCP announcements; Astera Labs is absent from the ESUN supporter list. UALink is effectively dead — Broadcom's SUE protocol has been donated as the baseline client-side protocol under ESUN. Amazon and AMD are dual-tracking (UALink vs. ESUN) but the author believes both will abandon UALink. This removes Astera Labs' switching content opportunity, which will be taken by Nvidia, Broadcom, Marvell, and others.

**Other notable items:** Bloom Energy (BE) showed supercapacitor-augmented 800V DC direct supply with modular reliability scaling — the author bought shares after seeing this. Pure Storage (PSTG) is being designed out by Meta in favor of next-gen QLC storage solutions. Multilane (private) is highlighted as a standout test equipment company solving backplane yield problems.

## Calls

- [[AVGO]] — LONG — n/a — CPO reliability data (zero failures, 2.5M hr MTBF) is best-in-class; strong endorsement of Broadcom's CPO platform
- [[MRVL]] — LONG — n/a — Alaska AEC is superior to Credo; 800G transceiver cycle drives massive revenue growth; author explicitly pitched long at conference
- [[CRDO]] — SHORT — n/a — Author explicitly pitched long MRVL / short CRDO; Marvell has a superior AEC product but cedes margin to Credo due to go-to-market passivity
- [[ALAB]] — SHORT — n/a — UALink is dead, ESUN replaces it; Astera Labs loses scale-up switching content to Broadcom and Nvidia
- [[BE]] — LONG — n/a — Author bought shares after seeing supercapacitor-augmented 800V DC direct supply; time-to-power advantage for datacenter deployments
- [[PSTG]] — SHORT — n/a — Meta is actively designing out Pure Storage in favor of next-gen QLC flash
- [[CIEN]] — MENTION — n/a — Nubis acquisition presented DWDM-based CPO approach; author strongly disagrees but respects the logic
- [[TSEM]] — MENTION — n/a — Accelink's SiPho-based CPO chip provides incremental content for Tower Semiconductor
- [[AMD]] — MENTION — n/a — Dual-tracking GPU scale-up between UALink and ESUN; OCP marketing own-goal with Nvidia transceivers in Helios rack demo
- [[NVDA]] — MENTION — n/a — CPO presentation showed no new data beyond GTC/Hot Chips; dual-sourcing transceiver DSP between internal and Broadcom
- [[FN]] — MENTION — n/a — Fabrinet mentioned only as example of misguided pod-monkey reaction to author's joke tweet; no real investment view
- [[002281.SZ]] — MENTION — n/a — Accelink showed impressive ELSFP optical power and stability at conference
- [[COHR]] — MENTION — n/a — Listed as viable 800G transceiver vendor; no specific investment view expressed
