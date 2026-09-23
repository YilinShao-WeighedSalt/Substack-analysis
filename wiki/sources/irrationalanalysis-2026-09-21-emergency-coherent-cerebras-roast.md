---
type: source
title: "[Emergency Memo] Coherent CPO/NPO Laser is Garbage + Cerebras Delusional Roast"
tags: [optics, cpo, lasers, linewidth]
related: ["[[irrationalanalysis]]", "[[COHR]]", "[[LITE]]", "[[CBRS]]", "[[silicon-photonics-interconnects]]"]
created: 2026-09-23
updated: 2026-09-23
authors: [irrationalanalysis]
year: 2026
url: "https://irrationalanalysis.substack.com/p/emergency-lunch-hour-market-memo"
venue: Irrational Analysis
post_date: 2026-09-21
tickers: [COHR, LITE, CBRS]
---

Rushed lunch-hour memo triggered by data from **ECOC** (the author is not attending; "little birds" relayed slides).

**Coherent's laser is proven garbage.** Coherent finally showed **phase-noise data** of its CPO/NPO/UHP/400mW laser — "provided the rope to hang themselves." Key argument: **linewidth** (β-separation linewidth = integral of phase noise above the β-separation line) comes in two forms — *intrinsic/instantaneous* and *effective*. Overlaying Lumentum's phase noise, Lumentum is **consistently better** and has no strange spike-cluster around 100 Hz (spikes far above the β-line are especially harmful). The author has measured the [[LITE]] UHP laser many times: effective linewidth **0.5–1.2 MHz**, intrinsic **10–50 kHz**. Coherent is "very obviously" reporting *intrinsic* linewidth instead of the (correct) *effective* one. Conclusion: **"100% proof" that Coherent's UHP laser catastrophically fails the 1 MHz effective-linewidth spec** of all standard NPO/CPO systems (incl. OCI MSA). "Nobody who is building a link cares about intrinsic linewidth."

**Cerebras integrated-laser photonics = "fantasy land bullshit."** E/O modulators (MZI, ring, EAM) are all thermally sensitive → no stable bias possible. "WAVEGUIDES ARE NOT LOW LOSS, FIBERS ARE." Link-budget math (32G NRZ): copper 0.1–0.2 dB/cm; Si waveguide ~0.5–1 dB/cm; SiN 0.2–0.5 dB/cm; fiber ~1.1 dB total for <100 m. Laser loss + waveguide loss + the heat burned biasing every modulator kills the design. Integrated laser "will never work in this situation."

## Calls
- **[[COHR]] — SHORT** — ECOC phase-noise slide reports intrinsic (not effective) linewidth; laser fails the 1 MHz effective-linewidth spec of NPO/CPO. px@call $310.39.
- **[[LITE]] — LONG** — superior, transparent phase noise; effective linewidth 0.5–1.2 MHz confirmed; the qual-only laser moat holds. px@call $945.67.
- **[[CBRS]] — SHORT** — integrated-laser wafer photonics physically impossible (thermal modulator bias + waveguide/laser loss blow the link budget). px@call $212.41.
