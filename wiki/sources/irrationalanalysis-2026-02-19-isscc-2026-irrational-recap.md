---
type: source
title: "ISSCC 2026 Irrational Recap"
tags: []
related: []
created: 2026-02-19
updated: 2026-02-19
authors: [irrationalanalysis]
year: 2026
url: "https://irrationalanalysis.substack.com/p/isscc-2026-irrational-recap"
venue: Irrational Analysis
post_date: 2026-02-19
tickers: [NVDA, LITE, MRVL, AVGO]
---

[[irrationalanalysis]] covers three ISSCC 2026 presentations with direct investment implications: Nvidia's co-packaged optics (CPO) die-to-die PHY, Celestial AI/Marvell's EAM-based optical transceiver, and MediaTek's 224G SerDes work.

**Nvidia (NVDA):** Nvidia presented results from TSMC COUPE — an optical extension of NVLink D2D using clock-forwarding over optics. The key achievement is extending a sub-2mm D2D PHY to 100+ meter reach at 1e-12 BER across all active lanes simultaneously, with 2.6 pJ/bit and ~1 ns latency. The author characterizes this as "the holy grail of communication systems" and estimates 18–24 months from lab to high-volume product. The Tx eye quality is described as unimpressive (3.6 dB extinction ratio vs. 5–9 dB for non-ring modulators), but the receiver design is highlighted as exceptional. Nvidia's choice of a slow-and-wide 32 Gbps NRZ lane architecture over 200 Gbps PAM4 is argued to reduce power and latency convincingly.

**Lumentum (LITE):** The Nvidia CPO system requires a tunable lab laser (Santec TLS-570) with 0.1 MHz linewidth and -145 dBc/Hz RIN — noise specifications the author argues only Lumentum can approach at the ~400 mW power class needed for CPO. Given the razor-thin amplitude margin in the Nvidia ring modulator Tx, the author argues Nvidia will be wholly dependent on Lumentum-quality lasers. The author states they are not adding to their existing LITE position only due to a self-imposed size limit above $400K market value.

**Celestial AI / Marvell (MRVL):** Celestial's GeSi EAM-based optical transceiver shows a TDECQ result below 1 dB, which the author calls "astounding," with total energy at 3.8 pJ/bit. However, the author flags potential "cheese" in the results: testing at a favorable 28°C, uncertain lane-activity conditions, and possible non-standard TDECQ tap count. The author also highlights internal contradictions in Celestial's presentation (attacking ring modulators while using ring filters for WDM) and estimates realistic EAM optical insertion loss at ~15 dB — significantly higher than competing modulators — due to thermal penalties from placement under the host ASIC. Despite caveats, the author states Celestial results are "incredible at best, very good at worst" and asserts 100% of Marvell's valuation should be derived from Celestial.

**MediaTek:** Described as presenting a literature review of others' work rather than original results. The author criticizes MediaTek's 224G SerDes for borrowing a flawed Intel idea (ADC-interleave gain) that forced use of two DFE taps, while simultaneously acknowledging that 1-tap is the practical limit. A sourced quote from a MediaTek employee calling 40 dB insertion loss compliance "very hard" is contrasted with Broadcom (AVGO) hitting 49 dB ~18 months ago and Nvidia passive copper channels likely at 50–55 dB.

## Calls

- [[NVDA]] — LONG — n/a — historic CPO breakthrough validates Nvidia's optical interconnect roadmap; 18–24 months to commercial deployment
- [[LITE]] — LONG — n/a — only vendor that can meet the extreme laser noise specs Nvidia's CPO system requires; author at position limit but would buy more
- [[MRVL]] — LONG — n/a — 100% of Marvell's valuation should be derived from Celestial; ISSCC results excellent even with caveats
- [[AVGO]] — MENTION — n/a — cited as SerDes benchmark; Broadcom hitting 49 dB insertion loss far exceeds MediaTek's capability
