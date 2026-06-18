---
type: source
title: "Huawei's Tau Scaling Law: Is the 'EUV Killer' Real?"
tags: []
related: []
created: 2026-05-29
updated: 2026-05-29
authors: [semidoped]
year: 2026
url: "https://www.semidoped.com/p/huaweis-tau-scaling-law-is-the-euv"
venue: Semi Doped
post_date: 2026-05-29
tickers: [ASML, BESI.AS, INTC, SNPS]
---
[[semidoped]] hosts a podcast episode in which Vik Sekar and Austin Lyons dissect Huawei's "tau scaling law" paper presented at ISCAS 2026 by HiSilicon head He Tingbo, which triggered viral claims that Huawei had rendered EUV and ASML obsolete.

**What tau scaling actually is.** The paper reframes chip performance around system-level delay (tau) rather than transistor geometry. Because Huawei cannot access EUV tools, it cannot shrink transistors further, so it proposes reducing tau across the entire stack — transistors, interconnects, memory protocols, network links, and software — by a factor alpha per generation (targeting ~1.3x/yr for mobile, ~1.5x for auto, ~10x for AI workloads). The hosts note the framing is intellectually sound but not entirely novel: it echoes STCO (system technology co-optimization) and Jensen Huang's "extreme co-design" philosophy.

**Logic folding via hybrid bonding.** The primary near-term technique is stacking two logic dies face-to-face using hybrid bonding at ~1.5 µm pitch — what Huawei calls "logic folding." This doubles transistor count in a given footprint without shrinking individual transistors. The Kirin 2026 mobile SoC is cited as demonstrated silicon. Challenges include thermal management, alignment precision, yield loss in die-to-wafer bonding, and the fact that logic-to-logic stacking is harder than memory stacking (no redundancy to route around defects). **BESI** (Netherlands) supplies a significant share of hybrid bonding equipment to China (~35% of recent quarterly revenue); hybrid bonding machines are not currently subject to the same export restrictions as EUV, though that could change.

**Impact on ASML.** The "EUV killer" framing is inverted: China was never buying EUV from ASML. Furthermore, logic folding requires manufacturing two DUV wafers per chip instead of one, which is net-positive for DUV machine demand, and EUV-enabled fabs that adopt stacking will further widen their performance lead over Huawei. The hosts are explicitly bullish on ASML as a result.

**Other tau knobs.** The paper also targets memory protocol fragmentation (unified bus to eliminate translation latency) and near-packaged optics / CPO (eliminating DSP latency in networking). These are seen as directionally correct but high-level.

**EDA and multiphysics.** The hosts flag **Synopsys** (and its Ansys multiphysics engine) as a key beneficiary: stacking active logic dies creates coupled thermal, mechanical, electrical, and optical simulation demands that will require next-generation EDA tooling. The EDA industry is already bullish given AI-driven license-per-agent pricing, and logic folding adds a new layer of complexity.

## Calls

- [[ASML]] — LONG — n/a — logic folding requires more DUV wafers per chip, and EUV-enabled fabs adopting stacking will widen their lead, making ASML a net beneficiary of tau scaling
- [[BESI.AS]] — LONG — n/a — dominant hybrid bonding equipment supplier with ~35% China revenue exposure; logic-on-logic stacking trend drives sustained demand for its machines
- [[INTC]] — MENTION — n/a — Intel Foveros Direct cited as a comparable logic-on-logic stacking capability that US fabs could deploy to leapfrog Huawei's tau scaling advantage
- [[SNPS]] — LONG — n/a — Synopsys/Ansys multiphysics EDA explicitly called out as bullish; logic folding creates coupled thermal, mechanical, and electrical simulation complexity that requires advanced EDA tooling
