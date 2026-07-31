---
type: theme
title: "Modular / Prefab 'LEGO' Datacenter Construction"
tags: [datacenter, construction, modular, prefab]
related: ["[[semianalysis-2026-07-29-lego-datacenters]]", "[[FIX]]", "[[STRL]]", "[[PWR]]", "[[FLEX]]", "[[SU.PA]]", "[[VRT]]", "[[datacenter-power]]", "[[ai-infrastructure-capex]]"]
created: 2026-07-31
updated: 2026-07-31
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
