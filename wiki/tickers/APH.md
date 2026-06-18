---
type: ticker
title: "APH — Amphenol"
tags: []
related: ["[[semianalysis-2024-07-17-gb200-hardware-component-supply-chain-bom]]", "[[semianalysis-2026-02-25-vera-rubin-extreme-co-design]]"]
created: 2024-07-17
updated: 2026-02-25
ticker: APH
current_stance: long
conviction: medium
last_review: 2026-02-25
---
## Call log
| date | publication | stance | px@call | thesis |
|------|-------------|--------|---------|--------|
| 2024-07-17 | [[semianalysis]] | MENTION | n/a | Primary source for NVLink Paladin HD backplane connectors; large volume beneficiary of Nvidia's copper-over-optical NVLink interconnect decision |
| 2026-02-25 | [[semianalysis]] | LONG | n/a | PaladinHD2 connectors displace internal cables; PCB area grows 2.3x, driving connector and substrate content sharply higher |

## Thesis evolution
Coverage opened in July 2024 as a structural mention within semianalysis's GB200 BOM teardown: Amphenol's Paladin HD backplane connectors were identified as the primary interconnect solution for NVLink, with the copper-over-optical decision at the rack level translating directly into high connector volumes per system. By February 2026 the view had firmed into an explicit long on the back of the Vera Rubin platform analysis: the shift to a cableless compute tray using PaladinHD2 board-to-board connectors eliminates the internal flyover cables that previously distributed signals, concentrating that interconnect content into Amphenol's connector products, while a 2.3x increase in PCB area simultaneously lifts substrate content per tray. Both publications are bullish; there is no bearish counterpoint in the covered sources. The conviction is held at medium rather than high because APH has appeared in only two notes and neither has provided a price-anchored entry thesis or discussed valuation.

## Outcome tracking
Neither call carries a px@call value, so quantitative outcome assessment is not possible. The thesis trajectory is consistently positive: the 2024 mention established Amphenol as a direct volume beneficiary of copper NVLink, and the 2026 upgrade to an explicit long reflects an architectural shift in Vera Rubin that structurally increases connector content per rack versus Blackwell rather than merely sustaining it. The live long thesis would be falsified by evidence that Nvidia reverts to optical or cable-based intra-tray interconnect in a future platform revision, or that a competing connector supplier displaces PaladinHD2 in Rubin qualification.
