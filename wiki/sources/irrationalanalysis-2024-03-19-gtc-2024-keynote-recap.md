---
type: source
title: "GTC 2024 Keynote Irrational Recap"
tags: []
related: []
created: 2024-03-19
updated: 2024-03-19
authors: [irrationalanalysis]
year: 2024
url: "https://irrationalanalysis.substack.com/p/gtc-2024-keynote-irrational-recap"
venue: Irrational Analysis
post_date: 2024-03-19
tickers: [NVDA]
---

[[irrationalanalysis]] provides a technical walkthrough of Jensen Huang's GTC 2024 keynote, arguing that Blackwell's architecture effectively obliterates virtually every AI chip startup and several cloud hyperscaler internal chip programs in one stroke.

The author opens with an explicit bias disclosure: NVDA is already half their portfolio, and they have no intention of selling a share. This frames the entire analysis as deeply bullish on NVDA.

The post proceeds through the keynote timestamps chronologically:

**NVLink 5th generation** (37:00): Blackwell's NVLink doubles bandwidth versus Hopper and now includes compute-in-network capabilities, expanding on the all-reduce functionality InfiniBand switches already offered. The author notes limited technical detail is publicly available but flags this as a significant moat-deepener.

**RAS (Reliability, Availability, Serviceability) engine** (37:00): Described as the most technically impressive innovation in the keynote. The new on-die RAS block continuously monitors every SRAM bit and every HBM bit connected to the chip — essentially embedding an Advanced Test Equipment (ATE) probe system directly on silicon. The author calls this "almost too good to be true" and notes ATE probing normally only happens at wafer-level before expensive packaging. Continuous in-field health monitoring at this granularity is unprecedented.

**Copper over optics** (45:00–49:00): Blackwell DGX uses passive copper cables for NVLink — 5,000 cables totaling 2 miles — saving 20KW versus an optical interconnect solution. The rack draws 120KW total, with water cooling inlet at 25°C and outlet at 45°C (2 liters/second). The author flags this as a significant thermal density problem: the 20°C delta and 120KW per rack means essentially no existing datacenter infrastructure can support Blackwell DGX without fully custom greenfield builds.

**Inference performance** (Blackwell vs. Hopper): The author corrects a misleading chart from the keynote, calculating a true 4.5x tokens/sec/GPU uplift from Hopper (~30 tokens/sec) to Blackwell (~135 tokens/sec) at comparable latency. FP4 performance of B200 is estimated to be even higher.

**Startup and hyperscaler impact**: The author's central thesis is that the breadth, integration depth, and manufacturing scale of Blackwell's announcement — combined with NVLink's scale, the compiler-driven inference optimization, and the RAS engine — makes it effectively impossible for AI chip startups or internal hyperscaler alternatives to compete on a full-system basis.

## Calls

[[NVDA]] — LONG — px@call n/a — Author holds NVDA as half their portfolio and refuses to sell; Blackwell's technical advantages in NVLink, RAS, and inference throughput reinforce the moat against all AI chip challengers.
