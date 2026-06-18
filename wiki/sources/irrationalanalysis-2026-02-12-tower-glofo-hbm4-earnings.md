---
type: source
title: "[Market Memo] Tower+GloFo Earnings, HBM4 Qualification Noise"
tags: []
related: []
created: 2026-02-12
updated: 2026-02-12
authors: [irrationalanalysis]
year: 2026
url: "https://irrationalanalysis.substack.com/p/market-memo-towerglofo-earnings-hbm4"
venue: Irrational Analysis
post_date: 2026-02-12
tickers: [TSEM, GFS, MU, NVDA, INTC]
---

This post from [[irrationalanalysis]] covers earnings reactions for Tower Semiconductor (TSEM) and GlobalFoundries (GFS), then pivots to an engineering-driven explanation of why HBM4 qualification noise is impossible to read from supply-chain sources alone.

## Tower Semiconductor (TSEM)

The author is long TSEM and holds $217K in short-term gains. The stock traded down on fears that the Intel breakup — Lip-Bu Tan backing out of a cleanroom deal — caps near-term upside. The author's view: Tower collects a nice breakup fee and simply raises prices while attributing the hike to Intel. The long-term thesis is intact: silicon photonics (SiPho) kills VCSEL at 200G/lane, GlobalFoundries' SiPho platform is weak, and Tower's partnership with Nvidia (likely for a new 1.6T SiPho transceiver targeting EML shortage) is a durable competitive moat. Intel backing out is characterized as actually bullish for Intel because it likely frees cleanroom space for advanced packaging. The author tried to sell covered calls but the bid/ask spread was too wide to bother.

## GlobalFoundries (GFS)

The author tried to buy puts on GFS before earnings but missed the fill. GFS popped 16% on the day. Reading the transcript live, the author concludes that ~80–90% of GFS SiPho revenue is Cisco/Acacia, that GFS's ring-assisted MZI technology is academically derived and inferior, and that GFS's recent acquisitions of minor SiPho players were a scramble to close the gap with Tower. The author has half the RF exposure of GFS, and much of Tower's RF exposure is Apple-related (Qorvo envelope tracker), which he views as higher quality. The post maintains a bearish/short bias on GFS.

## HBM4 Qualification Noise (MU / Samsung / SK Hynix / NVDA)

SemiAnalysis published a brief note claiming Micron failed Nvidia HBM4 qualification for the Rubin platform. Contradictory sell-side reports flew in both directions, with some claiming only Samsung passed and others claiming SK Hynix holds 70% share. The author argues the confusion is structurally inevitable due to four engineering factors: (1) high-speed probe stations are notoriously difficult to calibrate; (2) de-embedding probe S-parameters introduces measurement error; (3) contact capacitance variation corrupts results; (4) both Nvidia and the HBM4 vendors (Micron, Samsung, Hynix) hold hundreds of secret PHY tuning registers and must collaborate under conditions of asymmetric information. The conclusion is that supply-chain checks cannot reliably determine HBM4 qual status — the process is too iterative and opaque.

## Calls

- [[TSEM]] — LONG — n/a — Intel breakup fee + SiPho pricing power + Nvidia 1.6T transceiver deal keep long-term thesis intact despite near-term sideways drift.
- [[GFS]] — SHORT — n/a — GFS SiPho is inferior (ring-assisted MZI, ~80-90% Cisco/Acacia concentration), tried to buy puts pre-earnings.
- [[MU]] — MENTION — n/a — Subject of HBM4 disqualification rumor; author concludes uncertainty is structurally unresolvable via supply-chain analysis.
- [[NVDA]] — MENTION — n/a — Rubin CoWoS-L platform is the HBM4 qualification target; likely Tower SiPho transceiver customer for 1.6T design.
- [[INTC]] — MENTION — n/a — Backing out of Tower cleanroom deal framed as bullish for Intel (advanced packaging pivot) and net positive for Tower (breakup fee + pricing power).
