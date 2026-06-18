---
type: source
title: "Cerebras S-1 Initial Analysis"
tags: []
related: []
created: 2024-10-01
updated: 2024-10-01
authors: [irrationalanalysis]
year: 2024
url: "https://irrationalanalysis.substack.com/p/cerebras-s-1-initial-analysis"
venue: Irrational Analysis
post_date: 2024-10-01
tickers: [CBRS, NVDA, AMD]
---

[[irrationalanalysis]] provides an initial read of the Cerebras Systems S-1 filing ahead of the company's anticipated IPO under the ticker $CBRS. The post is structured as a rapid-fire takedown of the business, with the author flagging a trading strategy: buy the IPO pop driven by low float and hype, then short aggressively before lockup expiry.

**Gross margin weakness.** Hardware gross margins are reported at only 36%, which the author compares unfavorably to NVDA's ~75–80% hardware GM and AMD's 45–55%. Sub-40% GM in semiconductors is characterized as commodity-tier, on par with high-tier smartphone and laptop chips.

**Related-party revenue concentration.** The central bear argument is the extreme dependence on G42, a UAE state-affiliated entity and major investor. 87% of total Cerebras revenue (hardware + services) in the current year is from G42, and 97% of hardware revenue alone comes from G42. The author views the existing $1.4B contract and a dilutive stock option triggered by a single $500M order as a likely coordinated pump mechanism.

**Technical limitations.** The author argues the CS-3's proprietary memory-IO interface is slow and a fundamental bottleneck for both training and inference. As evidence, Cerebras still has not demonstrated support for Llama 3.1 405B — only the 8B and 70B variants — which the author attributes to SRAM inference being strangled by wafer I/O limits. Scaling multiple Wafer Scale Engines creates NUMA latency problems on training and bandwidth bottlenecks on inference.

**Competitive positioning is overstated.** The author asserts CS-3 competes with GB200 NVL36/72, not H100. A single GB200 NVL36 rack costs under $2M and draws ~65KW, versus an estimated $3–5M CapEx and ~120–140KW for five chained CS-3 units, giving NVDA a decisive TCO advantage. AMD's forthcoming MI325X, with large HBM capacity and aggressive pricing, is also expected to beat Cerebras in its inference niche.

**Trading thesis.** The author intends to seek IPO allocation, ride an initial pop fueled by retail enthusiasm and "gullible oil money," then build a short position backed by a detailed short report to be published between first earnings and the lockup expiry (~4–5 months post-IPO).

## Calls

- [[CBRS]] — SHORT — px@call n/a — plan to ride IPO pop then short aggressively; business is fundamentally weak with 97% hardware revenue from one related party, poor gross margins, and overstated technical capabilities
- [[NVDA]] — MENTION — px@call n/a — cited as the benchmark: ~75–80% hardware GM and GB200 NVL36/72 decisively beats Cerebras CS-3 on TCO
- [[AMD]] — MENTION — px@call n/a — MI325X highlighted as another competitive threat to Cerebras' inference niche with large HBM and low-margin pricing strategy
