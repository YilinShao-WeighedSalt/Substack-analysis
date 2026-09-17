---
type: source
title: "[Market Memo] Qualcomm/Amazon, Apple C2 Modem, Credo µLED, Cerebras I/O"
tags: [qualcomm, apple, modem, credo, uled, cerebras, serdes]
related: ["[[irrationalanalysis]]", "[[QCOM]]", "[[AAPL]]", "[[CRDO]]", "[[CBRS]]", "[[qualcomm-mobile-rffe]]", "[[cbrs-yield-short-vs-inference-tam]]", "[[qcom-short-vs-edge-ai-turnaround]]", "[[silicon-photonics-interconnects]]"]
created: 2026-09-17
updated: 2026-09-17
authors: [irrationalanalysis]
year: 2026
url: "https://irrationalanalysis.substack.com/p/market-memo-qualcommamazon-apple"
venue: Irrational Analysis
post_date: 2026-09-14
tickers: [QCOM, AAPL, CRDO, CBRS]
---

A deliberately low-effort "market memo" (author's words: "shitpost") stringing four minor-but-sharp topics.

**Qualcomm/Amazon deal.** IA reads it as backend physical-design services + bundled Alphawave 112G SerDes IP, specifically a **coherent-lite 800G optical DSP** that was already underway before Qualcomm bought Alphawave. Alphawave/Qualcomm is the only entity with good 112G SerDes on TSMC SF4X — an asset amid critical optical-DSP shortages — but 224G "has never shown evidence of functioning." Margins "likely low, much lower than the Apple modem margins this revenue is attempting to replace," and QTL revenue is "definitely going to be in jeopardy early next year." Deal was already in guidance; press-release timing looks aimed at drowning out Apple-modem news. (Aside: AWS once blacklisted Alphawave after "Tony did something to them on N7.")

**Apple C2 modem.** IA is "very surprised they got mmWave support in time for the QTL licensing cliff" — under-covered with massive implications. Original theory was a Verizon waiver to ship one year of non-mmWave iPhones; instead Apple is ahead of schedule and "fully self-sufficient now and can attack Qualcomm with little to no repercussion." Apple kept it under wraps and surprised QCOM management ~last month; QCOM's planned 20% share this year got slashed to low-single-digit (only contractual minimums). "Things are gonna get spicy in April 2027."

**Credo µLED 30-meter claim.** At the Goldman TMT conference the Credo CEO claimed 30-meter µLED reach. IA "calls bullshit" — even after fixing several unfixable problems, µLED hits massive chromatic + modal dispersion that caps reach; "no amount of DSP can make µLED work at 30-meter. MAYBE 10 meter." Demo expected at OCP.

**Cerebras I/O conspiracy.** After Hot Chips 2026 and talking to "JP," IA is now 100% confident the on/off-wafer I/O is a **direct extension of the NoC — a primitive parallel port**, which explains why Cerebras is defensive about it and why improving it has been "effectively impossible." NoC clock and external I/O doubled together in CS-3 (they are one and the same). Shoreline math: 2 edges × 21.5cm = 43cm; WSE-3 turbo total I/O = 2.4 Tbps → **0.0056 Tbps/mm** vs 1+ Tbps/mm for even a bad SerDes. Cerebras has partnered with **Skyechip** for custom interface IP; open question is whether next-gen serializes or stays a (better) parallel NoC extension, and whether it can use all four edges.

## Calls
- **[[QCOM]] SHORT $184.84** — low-margin Amazon deal replacing higher-margin Apple-modem rev; Apple C2 mmWave design-out + QTL cliff Apr-2027.
- **[[AAPL]] LONG $332.41** — C2 modem mmWave ahead of schedule; modem self-sufficiency + attack surface on Qualcomm.
- **[[CRDO]] SHORT $161.49** — 30-meter µLED reach claim physically implausible.
- **[[CBRS]] SHORT $190.47** — parallel-port wafer I/O at 0.0056 Tbps/mm; reaffirms activist yield short.
