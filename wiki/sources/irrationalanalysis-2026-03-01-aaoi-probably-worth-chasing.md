---
type: source
title: "AAOI Probably Worth Chasing"
tags: []
related: []
created: 2026-03-01
updated: 2026-03-01
authors: [irrationalanalysis]
year: 2026
url: "https://irrationalanalysis.substack.com/p/aaoi-probably-worth-chasing"
venue: Irrational Analysis
post_date: 2026-03-01
tickers: [AAOI]
---

[[irrationalanalysis]] opens by admitting frustration at having passed on AAOI in December after covering it, and states an intention to chase the stock the following week — assuming buying power survives anticipated macro volatility (the author holds crash puts over the weekend due to Iran-related geopolitical risk).

The core of the piece is a technical teardown of AAOI's earnings call transcript, focused entirely on qualification status rather than reported financials. The author frames AAOI as having a historically poor reputation for execution, then argues the company has quietly cleared the hardest hurdles for its 800G optical transceiver.

Optical qualification is broken into three stages: (1) reliability qualification per GR-468, (2) manufacturing line qualification, and (3) interoperability ("interop"). AAOI has completed the first two — which the author characterizes as the genuinely difficult parts — but stumbled on interop. The author is not alarmed by this, explaining in detail why interop failures are routine and often not the transceiver vendor's fault.

The technical argument centers on the IEEE 802.3ck standard governing 2x4x112G (800G) transceivers and the Tx FIR (finite impulse response) equalization procedure used during link training. During bring-up, the remote receiver iteratively requests coefficient adjustments from the local transmitter (pre- and post-cursor taps, e.g., c(-3) through c(1)). The standard mandates strict coefficient ranges and uniform step sizes. Nonlinearities from circuit PVT variation can cause the actual coefficient mapping to deviate from what the receiver expects, breaking link training without the transceiver being out-of-spec. The author's hypothesis is that AAOI's firmware has a Tx FIR coefficient mapping irregularity — consistent with the CEO's remark that the interop issue is "not our problem" (i.e., AAOI is within spec but a specific customer ASIC or switch chassis disagrees). This type of issue is described as common and fixable.

The bullish conclusion rests on three points: the hard reliability and manufacturing quals are done; the remaining firmware/interop issue is a normal and correctable problem; and AAOI has substantial internal InP (indium phosphide) laser capacity, which is strategically valuable in the current optical supply environment.

## Calls

- [[AAOI]] — LONG — px@call n/a — reliability and manufacturing quals complete; remaining interop issue seen as routine and fixable, with valuable internal InP capacity as upside
