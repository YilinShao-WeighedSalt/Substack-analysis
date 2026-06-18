---
type: source
title: "Inside the 800VDC Revolution Part 1"
tags: []
related: []
created: 2026-05-26
updated: 2026-05-26
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/inside-the-800vdc-revolution-part"
venue: SemiAnalysis
post_date: 2026-05-26
tickers: [NVDA, IFNNF, WOLF, ABBN.SW, ETN, VLTO]
---

[[semianalysis]] makes the case that the shift from 48–54V DC to 800VDC power distribution is a physics-driven inevitability for AI datacenters, not an optional upgrade. At rack densities approaching 660 kW–1 MW (e.g., Nvidia's Kyber Ultra class), 48V distribution requires ~12,500A and hundreds of kilograms of copper busbars; moving to 800VDC cuts current to ~750A, reducing resistive (I²R) losses by approximately 278×.

**Four-phase adoption model.** Phase 1 (2026–2027) deploys "power rack" sidecars in existing white space, converting 415V AC to 800VDC at the row level at a cost delta of ~$400–500k/MW, driven by Google and Meta pilots. Phase 2 (2027–2028) brings 800VDC-native compute (Kyber rack) with on-blade DC-DC conversion. Phase 3 (late 2028–2029) moves rectification to centralized grey-space units, eliminating per-row power racks and AC switchgear. Phase 4 (post-2029) deploys Solid-State Transformers (SSTs) converting directly from medium voltage to 800VDC at 98–99%+ efficiency versus ~82% for baseline AC architecture.

**Market sizing.** The sidecar/power-rack TAM peaks at ~$11B in 2028 before Phase 3 displaces it upstream; the SST TAM reaches ~$32B by 2030 at $1.25M/MW of content. Total datacenter electrical content stays in a $3.6–4.8M/MW band but shifts dramatically from grey-space switchgear and UPS toward power electronics and energy storage. Cumulative 800VDC-powered capacity is projected at ~39 GW by 2030.

**Efficiency gains.** Eliminating the central UPS in Phase 2 is the critical efficiency milestone, lifting cumulative power-chain efficiency from 83.7% to 86.5%. At 1 GW of IT load, Phase 2 saves ~58 MW of grid draw; Phase 4 (SST) saves ~69 MW—roughly the 5% improvement Nvidia claims.

**Winners.** Power-electronics suppliers benefit across all phases: Infineon (SiC modules, 12 kW BBU at 99.5% peak efficiency), Wolfspeed (10 kV SiC MOSFETs available March 2026). SST startups—DG Matrix (ABB-backed), Amperesand, Heron Power, Novos Power—have attracted over $320M in twelve months to March 2026. ABB, Delta Electronics, Eaton (acquired Resilient Power Systems, August 2025), Schneider Electric, and Vertiv are adapting product lines to 800VDC variants of busway, CDUs, and circuit breakers. Nvidia's MGX architecture embeds the voltage requirements; its October 2025 partnership with ABB (SACE Infinitus solid-state DC breaker, 1000V/2500A) reflects the ecosystem co-development.

**Losers.** Central UPS systems (2–3% conversion loss becomes uncompetitive), AC switchgear, and traditional low-voltage transformers face significant volume displacement in Phase 3 onward.

**Constraints.** NEC full 800VDC support is not expected until NEC 2032; pre-2029 deployments require case-by-case AHJ approvals. IEEE 1584 arc-flash models do not cover DC. A NERC Level 3 alert (May 2026) requires large datacenters to register as computational load entities and model their SST/BESS behavior for grid-stability studies.

## Calls

- [[NVDA]] — LONG — n/a — Architecture owner driving density requirements; MGX and Kyber rack designs embed 800VDC, creating a pull-through demand for the entire ecosystem
- [[IFNNF]] — LONG — n/a — Infineon supplies SiC power modules and BBU cards central to Phase 1–3 power-rack and on-blade conversion
- [[WOLF]] — LONG — n/a — Wolfspeed 10 kV SiC MOSFETs are a key enabling component for high-efficiency 800VDC conversion stages
- [[ABBN.SW]] — LONG — n/a — ABB is co-developing 800VDC busway, solid-state circuit breakers, and modular power blocks with Nvidia; DG Matrix SST startup is ABB-backed
- [[ETN]] — LONG — n/a — Eaton acquired Resilient Power Systems for SST expertise; well-positioned across circuit protection and power distribution for Phase 3 transition
- [[VLTO]] — MENTION — n/a — Vertiv adapting power and thermal products to 800VDC datacenter architecture; positioned as incumbent with risk of displacement if transition accelerates
