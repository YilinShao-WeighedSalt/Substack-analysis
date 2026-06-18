---
type: source
title: "OFC 2026 Irrational Recap"
tags: []
related: []
created: 2026-03-27
updated: 2026-03-27
authors: [irrationalanalysis]
year: 2026
url: "https://irrationalanalysis.substack.com/p/ofc-2026-irrational-recap"
venue: Irrational Analysis
post_date: 2026-03-27
tickers: [SMTC, LITE, MRVL, CRDO, AAOI, COHR, AVGO]
---

[[irrationalanalysis]] attended OFC 2026 and published a wide-ranging engineering-driven recap covering co-packaged optics (CPO), silicon photonics (SiPho), laser technology, and transceiver architectures, with direct investment implications for several names.

**VCSEL CPO:** The author is skeptical of VCSEL-based CPO/NPO. Furukawa's 200G/lane VCSEL demo showed an ~85% TDECQ failure rate across lanes — catastrophic eye quality. Lumentum's 32G NRZ/lane VCSEL NPO was described as mediocre due to aggressive over-peaking and electrical crosstalk from high lane density. Coherent's 100G/lane VCSEL CPO was considered the better approach. The author's preferred sweet spot is 64G NRZ or 112G PAM4 per lane for VCSEL NPO/CPO.

**Semtech CTLE:** The author has high conviction on Semtech (owns "a shit ton"), targeting 2–3x upside. A key thesis refinement at OFC: Semtech's analog amplifier (CTLE) lacks the multi-stage tuning knobs needed to rescue the Mediatek TPU, which the author now considers "absolutely cooked." This is not a negative for Semtech — the chip is useful across ACC copper cables, LPO, XPO, NPO, and traditional re-timed transceivers. Explicitly called out Macom as inferior to Semtech in analog amplifiers.

**Lumentum lasers:** Extremely bullish. Lumentum is the only vendor publicly disclosing laser linewidth specs for high-power (350–800 mW) DFB lasers. Wall-plug efficiency of ~13% at 30°C, with an 800 mW DFB at 0.1 MHz linewidth. The author argues that mass adoption of ring modulators (driven by Nvidia CPO) has made narrow linewidth critical for a rapidly expanding datacom market — a structural shift that creates a deep engineering moat for Lumentum. Received a $2B Nvidia investment on March 2, 2026, and quickly bought a fab to ramp. Author is not selling.

**Marvell:** Author is currently short for hedging purposes. Optical DSP market faces existential pressure from LPO, CPO, NPO, and Arista's XPO; new entrants (Broadcom, Credo, Cisco, Maxlinear) are taking share from Marvell's ~80% optical DSP dominance. Marvell appeared to be "throwing everything at the wall." Only reason not to go all-out short is Marvell's Celestial custom silicon franchise.

**Credo (CRDO):** Neutral despite an impressive interop demo. Credo operates in a 3–7 meter optical reach niche that shrinks as LPO/XPO/NPO/CPO proliferate. A strong Credo optical DSP is actually bearish Marvell, not bullish Credo.

**Broadcom/Meta CPO:** Updated CPO reliability data was presented and is bullish SiPho CPO overall. Minor hardware bug found (likely a capacitor issue in the ELSFP laser driver); this is exactly the kind of issue that extended pre-deployment testing is designed to catch. Broadly positive for the SiPho CPO roadmap.

**Tower vs. GloFo SiPho:** Tower Semiconductor's hybrid-bonded SiPho platform delivers ~110 GHz bandwidth vs. GloFo's fusion node at only 40–75 GHz with poor frequency response. GloFo fusion universally derided by every engineer the author has spoken with. Tower also has best-in-class SiN, integrated InP via Openlight, and integrated DFB/SOA/EAM.

**AAOI:** Transceiver performance at OFC was acceptable (~1e-12 pre-FEC for 800G, decent 1.6T). CPO laser effort noted but no linewidth/RIN disclosed — author uninterested without noise specs.

## Calls

- [[SMTC]] — LONG — n/a — owns heavily; dominant analog amp (CTLE) wins across LPO, XPO, NPO, ACC, and re-timed; Mediatek TPU loss is manageable, 2–3x target
- [[LITE]] — LONG — n/a — only vendor disclosing linewidth on high-power DFB lasers; ring-modulator CPO wave creates large new TAM for narrow-linewidth lasers; not selling
- [[MRVL]] — SHORT — n/a — short for hedging; optical DSP franchise under attack from LPO/XPO/CPO/NPO and new entrants; Celestial is the only offset
- [[CRDO]] — NEUTRAL — n/a — impressive demo but 3–7m niche structurally shrinks as advanced optics proliferate; good DSP is net-bearish Marvell not net-bullish Credo
- [[AAOI]] — MENTION — n/a — decent transceiver BER at 800G/1.6T; CPO laser exists but no linewidth/RIN disclosure limits conviction
- [[COHR]] — MENTION — n/a — received $2B Nvidia investment alongside Lumentum; OCS product has high insertion loss vs. Lumentum MEMS; playing catch-up on high-power laser with MOPA pivot
- [[AVGO]] — MENTION — n/a — strong internal laser team; Meta/Broadcom CPO reliability data presented positively; not a pure-play on narrow-linewidth CPO laser opportunity
