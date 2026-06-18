---
type: source
title: "Ampere Computing is probably dead."
tags: []
related: []
created: 2024-05-20
updated: 2024-05-20
authors: [irrationalanalysis]
year: 2024
url: "https://irrationalanalysis.substack.com/p/ampere-computing-is-probably-dead"
venue: Irrational Analysis
post_date: 2024-05-20
tickers: [ORCL, NVDA, INTC, AMD, ARM]
---

[[irrationalanalysis]] argues that Ampere Computing, a datacenter CPU startup founded in 2017 by ex-Intel engineers, is effectively finished as a going concern. The thesis rests on a single structural problem: every meaningful customer Ampere had has gone vertical on ARM-based silicon, leaving Ampere with no durable market to serve.

**Background.** Ampere's product pitch was "cloud-native" CPUs — ARM-based chips with predictable per-core clock speeds, linear core-count scaling, and low per-core power draw. These properties genuinely matter for public cloud virtualization (noisy-neighbor isolation across vCPU instances), and Ampere's products delivered on the claims. The problem is the market moved entirely around them.

**Customer attrition.** Microsoft and Google built custom ARM SoCs using ARM's Neoverse CSS chiplets (RTL licensing). Amazon (Graviton) has been self-sufficient for years. Nvidia Grace/GB200 NVL36/72 is rapidly taking share. On x86, Intel's Sierra Forest and AMD's Bergamo are credible responses in the same efficiency-core segment. Oracle is the sole remaining large customer — and only because it led multiple funding rounds, creating a captive relationship, not a competitive one.

**Technical stagnation.** Ampere's 2024 update video contained no meaningful microarchitecture disclosure on their claimed "cloud CPU" design or "AI features." Every serious competitor — AMD, Intel, Nvidia, ARM — publishes detailed technical specifications. Silence on architecture details, the author argues, signals there is nothing to disclose. The 256-core "AmpereOne" is described as a straight process shrink from TSMC N5 to N3E/N3P with no µarch improvement. ARM's upcoming Neoverse N4/V4 CSS chiplets are expected to beat Ampere at its own game by H2 2025, and existing CSS V3/N3 products may already do so — a point the author makes by noting Ampere has published zero TCO benchmarks against CSS chiplet products.

**Capital situation.** Ampere attempted an IPO in December 2022 but withdrew. With Oracle's balance sheet no longer open and no IPO proceeds, the author sees no plausible funding path to iterate to a competitive next-generation design.

**Conclusion.** Ampere entered a niche, validated it so thoroughly that hyperscalers and chip vendors all entered, and is now being squeezed out by both its former customers and incumbents simultaneously.

## Calls

- [[ORCL]] — MENTION — n/a — last major Ampere customer only due to captive investor relationship; no real competitive moat implied
- [[NVDA]] — MENTION — n/a — Grace/GB200 cited as rapidly expanding share in the efficiency-CPU datacenter segment
- [[INTC]] — MENTION — n/a — Sierra Forest and Clearwater Forest cited as strong competitive responses in Ampere's niche
- [[AMD]] — MENTION — n/a — Bergamo cited as already strong; Turin-Dense will further widen the gap
- [[ARM]] — MENTION — n/a — Neoverse CSS chiplets (RTL) expected to beat Ampere at its own game by H2 2025
