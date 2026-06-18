---
type: source
title: "ISSCC 2025: Ultra High-Speed SerDes"
tags: []
related: []
created: 2025-02-20
updated: 2025-02-20
authors: [irrationalanalysis]
year: 2025
url: "https://irrationalanalysis.substack.com/p/isscc-2025-ultra-high-speed-serdes"
venue: Irrational Analysis
post_date: 2025-02-20
tickers: [AVGO, 2454.TW]
---

[[irrationalanalysis]] reviews three SerDes presentations from ISSCC 2025, leading with an important caveat: all demos are run at artificially favorable conditions — room temperature (30–40°C die temp versus 90–110°C in production), cherry-picked typical-typical silicon, clean low-reflection channels, and over-built voltage regulators. The performance numbers shown are not representative of real-world production parts and should be interpreted with caution.

The central investment thesis concerns MediaTek's 212.5G SerDes built on TSMC N4. This is the design that failed in Google's TPU v6E selection, forcing Google to place an extra order for Broadcom's "inference-optimized" TPU v6P. The author had predicted MediaTek would fail on their first 224G-class attempt and was vindicated. However, reviewing the ISSCC presentation substantially upgrades the author's outlook for MediaTek's next attempt: the N3P design targeting TPU V7E.

Technical highlights of the MediaTek N4 SerDes: a two-tap FFE inserted into the final MUX (unusual, harms area, increases analog power, requires driver overbuilding); a 32-tap floating DFE in the receiver (judged excessive); capacitive gain in ADC-isolation buffers causing reflections; and fractional PLL jitter numbers that the author calls "insanely good" and "incredible." The JTOL test was run at 38 dB insertion loss rather than the correct 40 dB, and integrated phase noise was measured with extreme/favorable settings — caveats noted but not disqualifying.

Overall, the presentation moves the author's probability of MediaTek winning TPU V7E (late 2026) from ~30% to ~80%. The author recommends that investors bullish on Broadcom hedge by buying MediaTek (2454.TW), and argues that sell-side analysts are wrong to assign the full V7 win to Broadcom — multi-sourcing is the likely outcome starting late 2026 or early 2027. The author remains long Broadcom (recently bought more shares) and is not selling, viewing it as a strong long-term investment regardless of partial Google volume loss.

The third section covers a Korea+IBM FDM/OFDM 112G SerDes prototype that applies wireless QAM-OFDM techniques to wireline, requiring custom FPGA test infrastructure. The author considers it technically fascinating but of little near-term investment relevance.

## Calls

- [[AVGO]] — LONG — px@n/a — Author is personally long, recently added; sell-side is wrong assigning full TPU V7 win; expects multi-sourcing but views AVGO as a strong long-term hold
- [[2454.TW]] — LONG — px@n/a — Recommends institutional Broadcom bulls hedge by buying MediaTek; rates it the best Taiwanese investment; does not personally own due to brokerage limitations
