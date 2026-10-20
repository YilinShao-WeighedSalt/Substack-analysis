---
type: theme
title: "Modular / Prefab 'LEGO' Datacenter Construction"
tags: [datacenter, construction, modular, prefab]
related: ["[[semianalysis-2026-07-29-lego-datacenters, "[[semianalysis-2026-10-19-datacenters-2027-year-of-acceleration]]"]]", "[[FIX]]", "[[STRL]]", "[[PWR]]", "[[FLEX]]", "[[SU.PA]]", "[[VRT]]", "[[datacenter-power]]", "[[ai-infrastructure-capex]]"]
created: 2026-07-31
updated: 2026-10-20
status: emerging
first_seen: 2026-07-29
---
# Modular / Prefab 'LEGO' Datacenter Construction

## Plain-language explanation
Instead of building an AI datacenter brick-by-brick on site, operators increasingly **assemble it from factory-made blocks** bolted together on a poured foundation — concrete/steel shell panels, wired power rooms ("power skids/pods"), cooling skids (CDUs), and even complete "white-space" halls pre-fitted for racks. Two words get conflated: **prefabrication** = any part built off-site; **modular** = self-contained units (rooms/boxes/blocks) shipped complete and connected on site. Every modular unit is prefab; not all prefab is modular.

The driver is a **trade-labor shortage** capitalism can't quickly build past — electricians are 30-40% of DC construction man-hours, and SemiAnalysis projects an electrician shortage emerging in 2027 (worst in Texas, Ohio). Modular pulls repeatable work into factories running in parallel with sitework. SemiAnalysis's bottom-up model (50MW liquid-cooled US hall): modular compresses the build window **~36% (7-9 months faster)** and is **~8% cheaper per MW** — but the real prize is *speed = revenue* (a live IT-MW earns ~$0.5M/mo in stranded GPU depreciation alone, up to $50M/MW/yr on premium API deals).

## The modularization ladder (increasing factory scope)
1. **Component** — single factory-built piece of equipment.
2. **Skid** — components on an open frame, shipped as one package.
3. **Module** — a skid with walls/roof (e.g. a power room).
4. **Container** — a module in an ISO container (edge/low-latency; density-limited).
5. **Prefab DC block** — facility-scale, near-complete datacenter (Vertiv MegaMod, Crusoe Spark).

Shell evolution: precast concrete -> simplified single-story steel/PEMB halls -> purpose-built rapid-deploy (Meta's fabric "tents" at Prometheus; AWS narrow modular). Power/cooling are the most-modularized subsystems (Flex Anord Mardix power pods, Airedale/Modine CDUs, DG Matrix software-defined power routing, Karman CO2 heat-processing units).

## Who does the integration
- **Operator-led** (largest hyperscalers): AWS Project Houdini prefab white-space skids (partner Cupertino Electric = [[PWR]]); Aligned owner-furnished gear.
- **EPC / system-integrator-led** (vendor-agnostic): [[FIX]] Comfort Systems ("Modular Capex is the moat"), [[STRL]] Sterling, PCX, Nautilus, Bladeroom.
- **OEM-led** (full-stack, higher content capture): [[VRT]] Vertiv OneCore (~$3.5M -> ~$7M/MW), [[SU.PA]] Schneider EcoStruxure/turnkey.
- **Platform/reference**: Nvidia **DSX** — a validated AI-factory blueprint (compute+network+power+cooling+civil) delivered as an Omniverse digital twin (Max-Q token/W, Flex grid-services).

## Investment beneficiaries (SA, 2026-07-29)
Public: [[FIX]], [[STRL]], [[PWR]], [[VRT]], [[SU.PA]], [[FLEX]]. Private challengers: Infra Partners, Bladeroom, Faith Technologies, DG Matrix, Karman. SemiAnalysis estimates modular reaches **30%+ of live capacity by end-2028** (tracking 61GW+ / 1,000+ sites).

## Watch / falsifiers
Reliability doubts (operators/MEP contractors report modular hasn't always met claims — a failure risks the "precious hardware" and erases the time saved); double-margin penalty (module-vendor markup on top of integrator); transport/logistics limits (superload permits, insurance caps GPU shipments to 1-2 racks/trailer); commissioning (L2-L5 must happen on site, 3-8 months — the "single biggest gap"). Go-live only benefits if the *building* was the binding date vs power and GPU delivery.

## Timeline
- **2025-07:** SA first calls out Meta's fabric "tent" buildings.
- **2026-07-29:** SA "The Wild Wild West of LEGO Datacenters" — 80+ vendor universe, bottom-up cost/speed model, beneficiary breakdown.

### 2026-09-26 — China does the LEGO playbook at national scale (SemiAnalysis China Datacenter Model)
SemiAnalysis's new building-level China census (1,000+ facilities) shows the modular/prefab playbook the US is only now adopting has been China's standard for a decade (Tencent's 3rd-gen modular design dates to 2014). Key contrasts vs the US "Wild West of LEGO Datacenters": the US buildout is **power-gated** (interconnect queues, transformer lead times); **China is chip-gated** — power abundant, permitting a policy funnel (3-6mo vs US 12-13mo), labor plentiful. 100MW facility delivery compressed from ~18mo (cloud era) to **~12mo**; state-of-the-art faster. Methods: greenfield low-rise long-span **steel halls** (factory steel + on-site foundations, concrete only in the ground); **Alibaba CUBE 5.0 "100-day datacenter"** (30d factory + 50d install + 20d commissioning, ground-break-to-commissioning ~7-9mo, >10% cheaper than prior gen); Tencent **T-Block** full-modular containers. Full-modular is NOT the national default for two very-Chinese reasons: (1) cheap/abundant site labor makes the marginal container speed-gain small, and (2) colo developers pledge **real buildings** as bank collateral (a yard of containers appraises poorly). Capex a fraction of comparable US wholesale.

## 2026-10-20 — SemiAnalysis: +50GW in 2027, >$1T binding leases, "LEGO" buildout (preview)
**SemiAnalysis "Datacenters 2027" (Oct-19, paid preview)** forecasts **+50GW of datacenter capacity in a single year** (its +43GW/2027 number vs Brad Gerstner's "~25GW hunch") — essentially the entire cumulative global DC market through 2024, built in one year. The leading indicators behind it: **quarterly self-build construction starts "going parabolic"** (two hyperscalers driving) and **>$1T of binding/non-cancellable leases signed YTD 2026** (typically 15-20yr, $30-50B TCV/GW; leases lead debt raises lead buildout). Delivery is handled by the **modular "LEGO datacenter" movement**: **Google** modularized electrical architecture (prefab modules replace onsite cabling); **Meta** tent design; **AWS** simplified "SAMDC" shell + prefab data halls ("Project Houdini") → construction under 10 months and MEP labor down **up to 63%**; **DayOne** cut build timelines to ~9 months (~3GW leased since 2023). Power "broadly solved" via **behind-the-meter** generation (fuel cells, truck engines, refurbished turbines bypassing 5-10yr grid queues); the **ex-US buildout is sharply accelerating in 2027**. Open question (behind paywall): oversupply risk, and **memory/logic becoming the new #1 constraint in 2027-28**. SA named **Vertiv, ABB, Sterling Infrastructure** as order-surge beneficiaries → LONG [[VRT]]/[[STRL]]/[[ABB]]. → [[VRT]], [[STRL]], [[ABB]], [[datacenter-power]].
