---
type: source
title: "Datacenter Anatomy Part 2 - Cooling Systems"
tags: []
related: []
created: 2025-02-13
updated: 2025-02-13
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/datacenter-anatomy-part-2-cooling-systems"
venue: SemiAnalysis
post_date: 2025-02-13
tickers: [NVDA]
---

[[semianalysis]] provides a comprehensive technical breakdown of datacenter cooling infrastructure, covering everything from fundamental thermodynamics through hyperscaler-specific designs and the seismic shift driven by Nvidia's liquid-cooled GPU systems.

## Energy Metrics and Efficiency

The post opens with the two dominant efficiency metrics: Power Usage Effectiveness (PUE) and Water Usage Effectiveness (WUE). Industry average PUE sits at 1.6, while hyperscalers operate at 1.1–1.15. Google and Meta achieve roughly 1.10 PUE; Microsoft and AWS reach approximately 1.15. WUE is measured in liters per kilowatt-hour — a 50 MW datacenter at 60% utilization with 1.25 PUE and 2.0 WUE consumes approximately 657 million liters of water annually. Cooling systems account for 60–80% of non-IT electricity consumption.

## Cooling Architecture Taxonomy

The report maps a hierarchy from legacy air cooling (CRACs/CRAHs with raised floors) through modern Fan Walls (500–600 kW capacity, no raised floor required) and Rear-Door Heat Exchangers (RDHx, 30–50+ kW per rack). Water-cooled chillers dominate large facilities at up to 20 MW per unit with a coefficient of performance around 7x. Adiabatic cooling (water spray pre-cooling) boosts efficiency in high-ambient climates. The "Four Delta Ts" framework deconstructs air-temperature losses across the server, data hall, air handler, and mixing zones, showing how hot-aisle containment recovers significant efficiency.

## Hyperscaler Design Comparison

Each major hyperscaler takes a distinct approach. Microsoft's "Ballard" reference architecture (48 MW) eliminates chillers via direct evaporative cooling. Meta's "H" design targets 1.08 PUE and 0.20 WUE through free cooling with high inlet temperatures above 30°C, but requires 2–3 years to build. Google uses a waterside economizer with dual facility loops, achieving 1.10 PUE; its Belgian campus runs chillerless. AWS employs a free-cooling approach with exhaust fans and exterior louvers.

## Nvidia's Forcing Function

The most consequential finding is that Nvidia's GB200 NVL72 system — a 120 kW, 72-GPU rack — mandates Direct-to-Chip Liquid Cooling (DLC) and cannot be served by air cooling at all. This forces a datacenter-wide redesign across the industry. Thermal Design Power is trending toward 1,500 W chips "shipping next year," making the transition to liquid cooling structurally inevitable rather than optional.

## Supply Chain Implications

The post flags that liquid cooling demand is being systematically underestimated, with insufficient conversion-ready datacenter capacity. "Bridge" solutions with lower efficiency are expected to fill the gap. Even apparently simple components such as Quick Disconnects are already experiencing supply constraints, with supply chain impact varying sharply by vendor design choice.

## Calls

- [[NVDA]] — MENTION — px@n/a — GB200 NVL72 mandates industry-wide shift to Direct-to-Chip Liquid Cooling, making NVDA the primary forcing function for datacenter infrastructure redesign
