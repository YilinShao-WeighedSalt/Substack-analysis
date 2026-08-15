---
type: source
title: "Coherent Q4 FY26 Earnings"
tags: [optics, cpo, lasers, inp, vcsel]
related: ["[[irrationalanalysis]]", "[[COHR]]", "[[LITE]]", "[[AXTI]]", "[[silicon-photonics-interconnects]]", "[[co-packaged-optics]]"]
created: 2026-08-15
updated: 2026-08-15
authors: [irrationalanalysis]
year: 2026
url: "https://irrationalanalysis.substack.com/p/coherent-q4-fy26-earnings"
venue: Irrational Analysis
post_date: 2026-08-14
tickers: [COHR, LITE, AXTI]
---

Companion teardown to the Lumentum note: Coherent's call was "crap" and so were the numbers. Thesis — Coherent "financially self-immolates in the greatest optics bull market since the telco bubble," and the only explanation the finance people keep circling is bad yield. The "higher-transceiver-mix" excuse doesn't cover the miss.

- **CPO-laser skepticism.** Every sell-side analyst asks the same question different ways (Morgan Stanley pointedly: is the tiny GM expansion vs Lumentum from mix or 6-in yield?). Author: the numbers only make sense if yield is bad. PhotonLink (Coherent's VCSEL CPO/NPO brand) at **200G PAM4 on a VCSEL will fail GR-468 reliability** — the optimal VCSEL NPO/CPO datarate is 32G/64G NRZ; 200G forces heavy FEC/crosstalk mitigation and TIA-sensitivity burden, killing energy efficiency. "Coherent has great VCSELs (second only to Broadcom)" — but designing a 200G system is the wrong choice; the CPO dream is direct-drive (UCIe/clock-forwarded die-to-die SerDes) with no FEC, which you can't have at 200G PAM4/lane.
- **Margin mix cope.** Coherent's "we sell more than lasers" is the tell — Lumentum makes ~80% GM on the CPO laser while Coherent gets to sell isolators/FAU at ~30–40%.
- **6-inch InP conspiracy theory.** 6-in *should* yield better (better Aixtron MOCVD reactors, semi-modern ASML litho). So why is yield bad? Maybe the 6-in InP *wafers themselves* have poor uniformity — the best substrate supplier (AXTI) doesn't yet have 6-in InP (still R&D), so Coherent may be stuck with worse (Sumitomo) input goods. "Amusingly, Coherent's yield problems might not be their fault" — and once AXTI ships good 6-in InP, Coherent yield could finally rise.
- **Lumentum public CPO-laser data (contrast).** Praises Lumentum's OFC-grade public plots: WPE 13% in demo (30 °C, aggressive cooling) → ~10–11% realistic (40 °C die / 50 °C coldplate) vs 10% industry target; PCE 21–24% (target 25–30%, hit at 40 °C); **RIN averaging < −155 dBc/Hz vs −145 spec = >10× quieter**. DWDM CPO needs ±30 GHz (±0.17 nm) wavelength accuracy; process variation forces thermal tuning (~0.1 nm/K), which can push the TEC into inefficient reverse/heating mode near the coldplate temp — so high-power CPO-laser yield is "a nightmare" and a real moat. Coherent "could prove me wrong in a day" by publishing the same plots; it won't.

## Calls
- [[COHR]] — **SHORT** (px@call 325.83) — Call "crap," numbers worse; hides CPO-laser yield/noise data "because it's garbage"; 200G-PAM4 VCSEL fails GR-468; forced into low-margin isolators/FAU (~30–40%) while Lumentum earns ~80% on the laser.
- [[LITE]] — **LONG** (px@call 926.14) — Reiterated: only vendor publishing best-in-class RIN/linewidth/mode-hop data; ~80% GM CPO laser near-monopoly (with Broadcom).
- [[AXTI]] — **LONG** (px@call 81.64) — 6-in InP thread: Coherent's yield woes may be Sumitomo wafer-uniformity; once AXTI ships good 6-in InP, the whole chain's yield lifts. Pure-play InP substrate.
