---
type: source
title: "Practical Datacom Lasers"
tags: []
related: []
created: 2026-01-24
updated: 2026-01-24
authors: [irrationalanalysis]
year: 2026
url: "https://irrationalanalysis.substack.com/p/practical-datacom-lasers"
venue: Irrational Analysis
post_date: 2026-01-24
tickers: [LITE, INTC]
---

[[irrationalanalysis]] opens with a combative stance on Lumentum (LITE): ~17% short interest at time of writing, and the author holds LITE as his #2 position. He dares institutional shorts to press harder and predicts they will be "burnt to a crisp." The post is framed as an educational deep-dive into datacom laser physics designed to explain why LITE's moat is wider than the market appreciates.

**Two laser types dominate datacom.** VCSELs (Vertical Cavity Surface Emitting Lasers) emit light vertically, are cheap, and dominate 800G and below — but their direct-modulation architecture introduces "chirp" (correlated phase noise and amplitude non-linearity) that makes them unviable at 200G/lane (1.6T). DFBs (Distributed Feedback Lasers), where mirrors are embedded inside the gain medium, deliver far superior spectral purity and are the technology of record everywhere VCSELs fail: inside every EML, and as the external CW light source for all Silicon Photonics modulators (ring, MZI, EAM). VCSELs may survive in niche CPO arrays but the author views it as a terminal technology at high lane rates.

**CW lasers as imperfect Dirac deltas.** The author takes a signal-processing detour: an ideal CW laser is a perfect Dirac delta in the frequency domain (zero linewidth, zero RIN). Real lasers deviate through (1) linewidth — spectral broadening from electrical noise, driver ripple, and thermal drift; (2) relative-intensity noise (RIN) — amplitude fluctuations integrated from ~1 MHz to Nyquist, making RIN a data-rate-dependent spec; and (3) side-modes and mode hops — imperfectly suppressed spectral lines that cause instantaneous frequency jumps, accounting for the vast majority of transceiver link flaps in the field.

**Four noise amplifiers.** Higher output power amplifies every noise source. Electrical driver quality matters disproportionately — laser drivers require cleaner power than any GPU VRM, and money alone cannot solve it with switching regulators. Thermoelectric coolers (TECs) are mandatory for temperature stability to sub-0.01 °C precision per laser. Finally, epitaxy uniformity and grating/coupling design are binary: bad process yields unusable parts.

**The LITE moat.** Polarization-maintaining (PM) fiber — needed from laser to modulator — is expensive and a yield limiter; the industry wants to minimize it, which forces laser makers to push output power higher. Higher power makes all noise problems worse. The author challenges readers to find any Lumentum competitor publicly claiming linewidth specifications for high-power (300 mW+) DFB at O-band. He finds none, citing Lumentum's own product page for their External Laser Source (ELS) module. The implied conclusion: LITE is effectively a monopoly in high-power, narrow-linewidth O-band DFB — the critical component for 1.6T and CPO systems.

Intel (INTC) is noted as the author's #1 position; he explicitly states he is not selling despite separately being bearish on Intel Products division.

## Calls

- [[LITE]] — LONG — n/a — near-monopoly in high-power narrow-linewidth O-band DFB lasers; 17% short interest sets up a squeeze
- [[INTC]] — LONG — n/a — held as #1 position; thesis unchanged despite bearish view on Intel Products division
