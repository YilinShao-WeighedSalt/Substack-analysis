---
type: source
title: "Intel CPO Group is Alive? + NVDA/LITE/AEVA Bonus Papers"
tags: [intel, cpo, silicon-photonics, soa, rin, four-wave-mixing, lumentum, aeva, nvidia]
related: ["[[irrationalanalysis]]", "[[INTC]]", "[[LITE]]", "[[AEVA]]", "[[NVDA]]", "[[silicon-photonics-interconnects]]", "[[co-packaged-optics]]"]
created: 2026-08-21
updated: 2026-08-21
authors: [irrationalanalysis]
year: 2026
url: "https://irrationalanalysis.substack.com/p/intel-cpo-group-is-alive-very-interesting"
venue: Irrational Analysis
post_date: 2026-08-18
tickers: [INTC, LITE, AEVA, NVDA]
---

Stream-of-consciousness paper teardown (author rushing before Cerebras + Hot Chips). Concludes Intel's CPO/SiPho group is "maybe not completely dead."

**Intel CPO:** uses a hybrid-integration laser (gratings etched in silicon, Scintil-like) and an **SOA to amplify all 8 modulated wavelengths** — which spawns **four-wave-mixing (FWM)** noise and hurts RIN. Impressive ±10 GHz spacing accuracy and 16-wavelength array flatness, but he accuses Intel of **clipping spectra to hide FWM tones** and quoting BER off a perfect-timing bathtub curve. Against Nvidia's clock-forwarded "god-tier" bathtub curve (A+, BER 1e-12 at 0.47 UI), Intel's un-clock-forwarded result is a **"C+, maybe B-"**; at scale, FWM from two SOA stages (Tx + a stupid 3-cascaded-MZI Rx demux) makes it "a very ugly system."

**Nvidia/Lumentum paper (the "massive alpha"):** a monolithic **DFB laser array + per-channel SOA (MOPA array)** — each SOA sees one wavelength so **no FWM**. Excellent power flatness/spacing/SMSR, and Lumentum claims **0.5 dB coupling loss** and **only one isolator** (huge active-alignment/cost savings). But the monolithic array's **RIN is "garbage/unusable"** (~−137 dBc/Hz, one channel with a relaxation-oscillation spike). Net: validates Lumentum's *disaggregated* laser approach; monolithic integration isn't a threat.

**Aeva:** SOA paper referenced as per-channel SOA/beam-shaping optionality.

## Calls
- [[INTC]] — **NEUTRAL** @ $92.13 — CPO group alive but multi-λ SOA FWM = "C+" vs Nvidia; technically behind, not investable on this.
- [[LITE]] — **LONG** @ $879.28 — Nvidia/Lumentum ELSFP paper = "massive alpha"; 0.5 dB coupling + single-isolator moat, monolithic-array RIN unusable so integration won't erode Lumentum.
- [[AEVA]] — **NEUTRAL** @ $18.87 — per-channel SOA/MOPA optionality; author not positioned.
- [[NVDA]] — **NEUTRAL** @ $216.85 — Nvidia CPO "A+" clock-forwarded bathtub curve cited as the benchmark (technical praise, not a fresh stock call).
