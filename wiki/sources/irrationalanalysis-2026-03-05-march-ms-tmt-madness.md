---
type: source
title: "March [Morgan Stanley TMT] Madness"
tags: []
related: []
created: 2026-03-05
updated: 2026-03-05
authors: [irrationalanalysis]
year: 2026
url: "https://irrationalanalysis.substack.com/p/march-morgan-stanley-tmt-madness"
venue: Irrational Analysis
post_date: 2026-03-05
tickers: [LITE, COHR, MU, SNDK, BESI, ARM, INTC, AMD, NVDA, TSEM, AEHR, ON, STM, QCOM, AAOI, MRVL]
---

Written from the sidelines of the Morgan Stanley TMT conference (the author did not attend officially but networked extensively), this post is a wide-ranging intelligence dump from conversations with semiconductor investors and engineers. [[irrationalanalysis]] frames the piece as a collection of learnings from contacts, stressing transparency about his own long book to avoid perceptions of bias.

**Memory / HBM.** The author pushes back on the idea that Groq-style LPU architectures will destroy HBM demand. SRAM scaling is effectively dead post-3nm, leading-edge logic wafer supply is severely constrained, and SRAM simply cannot cover most inference workloads — fears of HBM demand destruction are labelled a "stupidity singularity" reminiscent of the Deepseek panic, with potential for dumb temporary price action in SK Hynix, Samsung, and Micron. High-Bandwidth Flash is dismissed as fundamentally broken: QLC NAND took 5.5 years to reach mainstream and still suffers from endurance (0.41 DWPD) that makes permanently attached flash in advanced packaging idiotic. On NAND vs. DRAM, the author slightly prefers NAND because engineering insights (QLC co-design) can create alpha; Sandisk and Kioxia are tied for first in QLC execution; shoutout to Hans Mosesmann for being right on the NAND thesis a year early.

**Groq.** A key technical assumption — optical clock forwarding as the performance differentiator — was corrected by an engineer; the sync penalty is negligible. Author remains bullish but now frames Groq as an orthogonal, high-margin, low-latency inference product line (like a sports bike alongside GPU trucks), not a threat to GPU demand.

**Hybrid Bonding (BESI).** HBM4 pin-speed drama (Nvidia pushing 11 Gbps vs. JEDEC 8 Gbps spec) is partly a signal-integrity problem caused by micro-bump parasitics; hybrid bonding would have prevented it and should accelerate adoption.

**Agentic CPU.** Bullish on CPU broadly. ARM is complicated by Masa's likely use of shares as loan collateral. AMD CPU is excellent but GPU uncertainty makes it hard to play. Intel Products is a long-term zero in the author's view; the position is pure foundry optionality on 18A ramping 2027.

**Tower Semi.** Shifted from bearish to neutral on CPO share. At lower speeds (below 200G PAM4), Tower's 65nm EIC with silicon-nitride/undercut/hybrid-integration features (Openlight) becomes a credible alternative to TSMC's COUPE.

**Nvidia valuation.** Described as "comically cheap" at ~17x forward P/E while optics names trade at high multiples — the author calls this a collective action problem among buyside.

**Semicap.** Remains constructive; views it as the most balanced risk/reward sector as Samsung Foundry and Intel Foundry absorb spillover orders.

**Power Semis.** Sector generally disliked (fungible, price-elastic). Bought some ON Semi for DD purposes; ON and STM described as the only non-shitcos in the space.

**Android/Smartphone.** Apple is increasing iPhone base memory spec while holding price flat, actively taking share from Android OEMs; double-negative for Qualcomm (losing Apple socket and Android share simultaneously).

**Obscure Optics.** AAOI: maintains opinion, management confirmed interop/Tx FIR fix is in place. Aixtron: good, beaten up by SiC/EV cycle but new 6-inch InP tool generation is strong as Lumentum and Coherent need more epi capacity after Nvidia's $2B investments in each. Nokia/Infinera: possible sleeper datacenter re-rating via 6-inch InP capacity.

**MRVL Puts.** Snapshot shows MRVL puts going to zero, backing out ~$23K from P&L.

## Calls

- [[LITE]] — NEUTRAL — px@n/a — Nvidia's $2B investment doesn't change engineering view; linewidth/noise fundamentals unchanged
- [[COHR]] — NEUTRAL — px@n/a — Same as Lumentum; $2B Nvidia investment noted but no change to engineering view
- [[MU]] — MENTION — px@n/a — Risk of GTC-induced dumb price action if HBM demand fears spike; no directional call stated
- [[SNDK]] — LONG — px@n/a — Best-in-class QLC co-design tied with Kioxia; preferred NAND play over DRAM
- [[BESI]] — LONG — px@n/a — HBM4 signal-integrity drama should accelerate hybrid bonding adoption
- [[ARM]] — MENTION — px@n/a — Bullish on CPU theme but complicated by Masa's collateral dynamics; no clear directional call
- [[INTC]] — LONG — px@n/a — Dead money near-term; pure foundry/18A optionality play, products valued as long-term zero
- [[AMD]] — MENTION — px@n/a — CPU is excellent but GPU uncertainty makes it too hard to play
- [[NVDA]] — LONG — px@n/a — Comically cheap at ~17x forward P/E; Groq is orthogonal, not cannibalistic
- [[TSEM]] — NEUTRAL — px@n/a — Shifted from 0% to neutral CPO share view; lower-speed PIC design space becoming credible
- [[AEHR]] — MENTION — px@n/a — Discussion of wafer-level burn-in for leading-edge logic; no conclusion yet
- [[ON]] — LONG — px@n/a — Bought for DD; one of only two non-shitcos in power semis alongside STM
- [[STM]] — MENTION — px@n/a — Named as one of two quality names in power semis
- [[QCOM]] — SHORT — px@n/a — Double share loss: losing Apple socket and Android OEM share simultaneously
- [[AAOI]] — LONG — px@n/a — Interop/Tx FIR fix confirmed by management; maintains positive view
- [[MRVL]] — SHORT — px@n/a — MRVL puts in book; puts going to zero per trading snapshot note
