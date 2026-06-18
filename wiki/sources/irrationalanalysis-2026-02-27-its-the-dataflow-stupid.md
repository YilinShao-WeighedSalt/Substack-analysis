---
type: source
title: "[unfinished draft] It's the dataflow, stupid."
tags: []
related: []
created: 2026-02-27
updated: 2026-02-27
authors: [irrationalanalysis]
year: 2026
url: "https://irrationalanalysis.substack.com/p/unfinished-draft-its-the-dataflow"
venue: Irrational Analysis
post_date: 2026-02-27
tickers: [NVDA]
---

[[irrationalanalysis]] publishes an unfinished draft arguing that Nvidia's ~$20B acquihire of Groq is more transformative than its 2020 Mellanox acquisition — a full reversal from years of publicly dismissing Groq's architecture. The post is explicitly incomplete: sections on Cerebras, SambaNova, Etched, MatX, Taalas, Positron, and D-Matrix are all placeholder `<todo>` stubs, pending negotiations with those startups for technical access and publication permission. Only the Groq and architecture-primer sections are substantively written.

The author builds a four-axis framework for comparing AI chip architectures: (1) memory hierarchy (cache vs. scratchpad), (2) memory access/routing via network-on-chip (ring, mesh, crossbar), (3) compute structure (SIMD warps, VLIW bundles, systolic arrays), and (4) chip-to-chip topology (all-to-all, 3D-torus, dragonfly). This framework is applied to AMD Genoa-X, Intel Sapphire Rapids, Nvidia Blackwell Ultra (GB300), and Google Ironwood TPU as "normal" reference architectures before pivoting to Groq.

Groq is described as a 144-wide VLIW dataflow machine with a pure scratchpad SRAM model and no DRAM — acknowledged as such by Groq's own chief architect Dennis Abts at Hot Chips 2022 before Abts departed for Nvidia. The compiler must statically schedule every instruction at cycle-level granularity and synchronize every chip across every rack simultaneously. Any clock skew or PPM drift halts execution. The author had attacked this design for years, but now argues: after 6+ years hardening their compiler via a money-losing inference cloud, Groq has crossed a threshold. More importantly, Nvidia now holds the IP to fix Groq's core pathologies.

Four specific Nvidia IP synergies are enumerated: (a) clock-forwarded SerDes over optics — presented at ISSCC, achieving ~16 ps jitter, orders of magnitude better than Groq's counter-based sync scheme, directly addressing the synchronization brittleness; (b) hybrid bonding to expand the SRAM scratchpad with minimal latency penalty, an option Groq lacked the resources to pursue; (c) Nvidia's world-class liquid cooling and thermal design teams, able to eliminate the hotspot underclocking Groq likely suffered; (d) a theoretical optical global clock distributed across racks, which would be uniquely transformative for Groq-style deterministic dataflow at datacenter scale.

The author holds a large position in Nvidia shares and call options disclosed in the post and frames the $20B price as justified precisely because it was high enough to foreclose negotiation — getting Groq talent inside Nvidia offices within four business days of the announcement. The bribery theory (connecting Don Jr.'s 1789 Capital to a recent Groq funding round) is explicitly rejected on valuation grounds: $20B is far too expensive to be a political payoff.

## Calls

- [[NVDA]] — LONG — n/a — Groq acquihire is bigger than Mellanox; Nvidia's clock-forwarding, hybrid bonding, and thermal IP can unlock the full potential of Groq-style dataflow architecture, making this a transformative deal worth the $20B price.
