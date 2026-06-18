---
type: source
title: "SerDes Wars: Maybe MediaTek TPU Can Be Salvaged by... Semtech"
tags: []
related: []
created: 2025-12-15
updated: 2025-12-15
authors: [irrationalanalysis]
year: 2025
url: "https://irrationalanalysis.substack.com/p/serdes-wars-maybe-mediatek-tpu-can"
venue: Irrational Analysis
post_date: 2025-12-15
tickers: [SMTC, AVGO, 2454.TW]
---

[[irrationalanalysis]] argues that Semtech's ACC (Active Copper Cable) linear equalizer chip may be the key to making MediaTek's otherwise flawed TPU SerDes competitive against Broadcom's offering. The post is triggered by Taiwan rumor-mill chatter suggesting Google is considering MediaTek for its next TPU, which the author initially dismissed as Google negotiating leverage against Broadcom but then reconsidered.

The technical crux is the CTLE (continuous-time linear equalizer): a type of amplifier placed in the signal path on PCBs or cables to compensate for channel loss at high data rates. The author explains the engineering tradeoffs carefully — all amplifiers add noise, performance degrades with higher data rates, and there is a placement sweet spot relative to the SerDes Tx. Too close causes saturation; too far and the amplifier's own noise overwhelms the benefit. A trusted contact told the author that Semtech's CEO is actively promoting using the ACC chip on PCBs, not just in cables — a significant signal.

MediaTek's N4-node SerDes design, first shown at ISSCC 2025, has two serious flaws: (1) it uses two DFE taps instead of one, which dramatically worsens DFE-propagation burst errors, and (2) it adds gain to the ADC interleaves (~8 dB), which is unconventional and likely the reason the 32-tap floating DFE was required to cancel out sampling error. The author's theory is that MediaTek could remove the ADC gain, remove the extra DFE tap, and rely instead on blanket Semtech linear equalizers across the PCB and ACC cables to compensate for channel loss — potentially making the chip viable. The key caveat: the author cannot verify this theory without Semtech's GN8112 (112G) or 224G datasheets, which Semtech refuses to share publicly or via their portal.

Competitive dynamics: Semtech faces no real competitor in this space since Macon is characterized as inadequate, making Semtech a single-source supplier. Google reportedly plans to use Semtech ACC for 200G per lane in 2027. If the MediaTek theory holds, Semtech becomes a critical enabling layer for any hyperscaler choosing a non-Broadcom SerDes path.

## Calls

- [[SMTC]] — LONG — n/a — Sole-source supplier of ACC linear equalizers that could enable MediaTek TPU SerDes to compete with Broadcom; Google 200G/lane 2027 design win cited
- [[AVGO]] — MENTION — n/a — Referenced as the gold standard for SerDes that MediaTek and Google are trying to move away from
- [[2454.TW]] — MENTION — n/a — MediaTek TPU SerDes has identified design flaws (dual DFE tap, ADC gain) that Semtech ACC may compensate for
