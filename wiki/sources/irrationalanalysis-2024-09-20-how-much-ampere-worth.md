---
type: source
title: "How Much is Ampere Computing Worth?"
tags: []
related: []
created: 2024-09-20
updated: 2024-09-20
authors: [irrationalanalysis]
year: 2024
url: "https://irrationalanalysis.substack.com/p/how-much-is-ampere-computing-worth"
venue: Irrational Analysis
post_date: 2024-09-20
tickers: [ARM, ORCL, INTC, AMD]
---

[[irrationalanalysis]] argues that Ampere Computing is a deeply impaired asset worth approximately $75M — a tiny fraction of the ~$800M invested into it — and that its situation is essentially terminal. The post begins with an explainer on how ARM (the corporation) monetizes its IP through Architectural License Agreements (ALAs), Technology License Agreements (TLAs), Total Access subscriptions, Flexible Access subscriptions, and the Neoverse Compute Subsystem (CSS) chiplets. This taxonomy is critical because it explains the exact mechanism by which Ampere's customers (Microsoft Cobalt, Google, Amazon, etc.) have migrated away: they ported their software from x86 to ARM ISA using Ampere's chips, then transitioned to ARM's own CSS chiplets or custom designs, rendering Ampere obsolete.

Ampere Computing, founded in 2017 by ex-Intel executives including Renee James, had early success with a "cloud-native" manycore CPU story. A Softbank-proposed valuation of $8B was floated in 2022, but a planned IPO was abandoned as revenue collapsed. Oracle is the last meaningful customer and a major investor; due to Renee James sitting on Oracle's board, ORCL is legally required to disclose related-party transactions. The author treats Oracle's ongoing investment as evidence of trapped capital rather than strategic value — Oracle gains nothing incremental from a full acquisition since they are already Ampere's sole revenue source and have locked in support contracts through 2030.

On assets, Ampere holds a custom ARM V8.6 CPU core (already behind the curve vs. V9), a proprietary software stack, and some IP novelties like a low-overhead memory tagging implementation. On liabilities: ~1,500 employees (the author estimates 30% immediate cuts post-acquisition), prepaid Oracle chip contracts, mandatory support obligations through 2030, and critically, an ALA that is likely non-transferable (per precedent set in the Qualcomm/Nuvia lawsuit). The author's valuation framework benchmarks Ampere against the cost of an ARM Total Access annual subscription, concluding the company is worth $75M.

## Calls

- [[ARM]] — MENTION — n/a — Core licensor whose Total Access subscription serves as the valuation benchmark for Ampere's IP
- [[ORCL]] — SHORT — n/a — Oracle is trapped holding heavy bags in Ampere; has no incentive to acquire outright and is Ampere's captive sole customer, signaling poor capital allocation
- [[INTC]] — MENTION — n/a — Named as exclusive x86 ISA holder alongside AMD, contextual only
- [[AMD]] — MENTION — n/a — Named as exclusive x86 ISA holder alongside Intel, contextual only
