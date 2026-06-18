---
type: source
title: "Micron FQ4 2025: MEETHINKS YOUSSA DOTH PROTEST TOO MUCH"
tags: []
related: []
created: 2025-09-26
updated: 2025-09-26
authors: [irrationalanalysis]
year: 2025
url: "https://irrationalanalysis.substack.com/p/micron-fq4-2025-meethinks-youssa"
venue: Irrational Analysis
post_date: 2025-09-26
tickers: [MU, 000660.KS, 005930.KS]
---

[[irrationalanalysis]] dissects Micron's FQ4 2025 earnings call and callback, arguing that Micron's management engaged in a carefully worded but ultimately misleading defense of their HBM4 position after NVIDIA raised the speed bar to 11 Gbps per pin — well above the official JEDEC spec of 8 Gbps.

**The Core Engineering Indictment**

The author's central claim is that Micron made a catastrophic decision to build their HBM4 base die on an internal CMOS process node derived from a DRAM process rather than a dedicated logic foundry node (as SK Hynix and Samsung did). DRAM process nodes are optimized for capacitor density, not transistor speed, making them inherently inferior for high-frequency logic applications. This decision was apparently made to save cost.

When NVIDIA raised the HBM4 speed requirement from 8 Gbps (4 GHz Nyquist) to 11 Gbps (5.5 GHz Nyquist), Micron's yield on their DRAM-node base die would have collapsed. The author uses a detailed explanation of parametric yield and Shmoo plots to illustrate that while Micron management truthfully stated they had delivered 11 Gbps samples to NVIDIA, cherry-picking the top few percentile of the yield distribution for samples does not imply economically viable production yield. The author concludes Micron's HBM4 yield at 11 Gbps is economically unviable, and that management's repeated, anxious invocation of "11 Gbps" across both calls betrays deep internal panic.

**Earnings Call Behavior**

The author observes that management (CEO Sanjay Mehrotra and others) proactively brought up "11 Gbps" multiple times without being directly asked, and repeated talking points compulsively — behavior the author reads as signs of extreme nervousness rather than confidence. The callback (a rare second sell-side call) was characterized as an attempt to suppress further "chatter."

**Competitive Context**

SK Hynix is described as having delivered qualifying HBM4 at 11 Gbps. Samsung's status is contested. Micron's locked-out status could force them to wait for HBM4E, ceding the current HBM4 cycle to competitors. A traditional DRAM shortage/demand cycle could still bail out Micron's stock even if HBM4 is a disaster, hence the author's official rating: ¯\_(ツ)_/¯.

**Author Bias Disclosure**

The author closed all Micron options positions before earnings (avoiding IV crush) and states no current position or directional view on MU stock or options.

## Calls

- [[MU]] — NEUTRAL — px@n/a — HBM4 base die built on DRAM process node is a self-inflicted engineering disaster; 11 Gbps yield almost certainly unviable, but traditional DRAM cycle could rescue the stock regardless
- [[005930.KS]] — MENTION — px@n/a — Samsung's HBM4 qualification status described as contested; may also be struggling to meet 11 Gbps requirement
- [[000660.KS]] — MENTION — px@n/a — SK Hynix cited as having successfully delivered 11 Gbps HBM4 using a proper logic process node for base die, positioning them as the clear HBM4 winner
