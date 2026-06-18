---
type: source
title: "Thanksgiving Thoughts: TPU VS NVDA, AVGO, MediaTek, Intel Foundry"
tags: []
related: []
created: 2025-11-28
updated: 2025-11-28
authors: [irrationalanalysis]
year: 2025
url: "https://irrationalanalysis.substack.com/p/thanksgiving-thoughts-tpu-vs-nvda"
venue: Irrational Analysis
post_date: 2025-11-28
tickers: [NVDA, AVGO, INTC, SITM, BE, GFS, 2454.TW]
---

[[irrationalanalysis]] covers four topics in this Thanksgiving post: the Google TPU vs. Nvidia GPU discourse, the persistent MediaTek TPU rumors, Intel Foundry's packaging opportunity, and a trading account update.

**NVDA / TPU vs. GPU discourse.** The author dismisses the growing "TPUs will kill Nvidia" narrative as a "stupidity echo chamber," noting nothing has changed on the engineering side. In long-only accounts, NVDA remains the largest position. The trading account carries zero Nvidia exposure, but the author would buy 200/220c calls ~6 months out if the stock hits $160, and double down at $150.

**AVGO / MediaTek TPU FEC analysis.** Taiwan's rumor mill has repeatedly predicted a large volume shift of Google TPU sockets from Broadcom to MediaTek. The author debunks this with a detailed technical argument. The crux: hyperscalers now want half RS-FEC to cut latency, which tightens error budgets (≤5 burst errors/packet in practice). Concatenated ("inner-outer") FEC — the feature rumored to give MediaTek an edge — only helps when burst errors are absent. MediaTek's 200G SerDes design retains a second DFE tap and gain in ADC interleaves, making it far more vulnerable to burst errors than Broadcom's implementation. The author concludes Broadcom is "safu" for the primary TPU socket; MediaTek might capture limited volume on a simple prefill-optimized TPU with benign PCB channels. The prediction from summer 2025 proved correct: MediaTek TPU was delayed and volume slashed.

**INTC / Intel Foundry packaging.** The author argues Intel Foundry's real advantage is advanced packaging (EMIB), not leading-edge logic. TSMC deliberately built zero advanced packaging capacity outside Taiwan — a strategic gap Intel can exploit. Lip-Bu Tan has cleaned house and poached a competent TSMC executive. The author treats EMIB and CoWoS-L as functionally equivalent from a signal-integrity standpoint. An 18A packaging order has materialized. INTC calls are held until assignment; the author won't trim until INTC trades at least 2× the P/B of GFS.

**Other positions.** The author is waiting for wash-sale periods to expire before re-entering SITM and BE.

## Calls

- [[NVDA]] — LONG — n/a — Largest long-only position; would add calls at $160 and double down at $150 despite zero trading-account exposure
- [[AVGO]] — LONG — n/a — Broadcom is "safu" for primary Google TPU socket; MediaTek's SerDes architecture makes it uncompetitive
- [[2454.TW]] — SHORT — n/a — MediaTek TPU repeatedly delayed and volume slashed; DFE-tap design makes SerDes prone to burst errors and unsuitable for primary TPU socket
- [[INTC]] — LONG — n/a — Holding calls to assignment; Intel Foundry's EMIB packaging is the real competitive moat once Lip-Bu Tan completes the cleanup
- [[GFS]] — MENTION — n/a — Used as valuation benchmark; author targets INTC at 2× GFS P/B before trimming
- [[SITM]] — LONG — n/a — Waiting for wash-sale period to expire before re-buying
- [[BE]] — LONG — n/a — Waiting for wash-sale period to expire before re-buying
