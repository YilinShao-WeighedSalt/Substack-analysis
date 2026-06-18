---
type: source
title: "Power as the Next Physics Wall for AI"
tags: []
related: []
created: 2026-05-08
updated: 2026-05-08
authors: [semidoped]
year: 2026
url: "https://www.semidoped.com/p/power-as-the-next-physics-wall-for"
venue: Semi Doped
post_date: 2026-05-08
tickers: [COHR, NVDA, TXN, NVTS]
---

[[semidoped]] hosts Vik Sekar (Vik's Newsletter) and Austin Lyons (Chipstrat) for a deep dive into why power delivery is becoming the next physics-constrained bottleneck in AI infrastructure — the same way resistance in copper interconnects forced the industry toward optics.

## Core Argument

Pre-AI cloud racks drew ~10–15 kW each. Current AI accelerator racks run 100–120 kW. NVIDIA's Kyber-generation racks (Rubin Ultra) are rated at **600 kW**, with a clear roadmap toward **1 MW per rack** — a 100x increase over the cloud era. At the incumbent 48V DC rack standard (Meta-standardized), 600 kW demands **12,500 amps of current**. Because resistive losses scale as I²R, even tiny connector or bus resistance dissipates enormous heat at kiloamp-scale current — the identical physics (resistance as the binding constraint) that drove the industry from copper interconnects to indium phosphide optics.

## The 800V Solution

The answer mirrors the optics transition: raise the voltage. At **800 V**, the same 600 kW requires only ~750 A — roughly a 16× current reduction that cuts resistive losses by 100–200× (squared relationship). 800 V is not arbitrary: the EV industry has already ruggedized IGBTs and wide-bandgap semiconductors (silicon carbide, gallium nitride) to operate at this level under harsh thermal conditions. NVIDIA is exploring 800V architectures. The analogy to co-packaged optics (CPO) applies directly: just as CPO pushes the electrical-to-optical conversion as close to the chip as possible, **vertical power delivery** pushes high-voltage conversion to the point of load — minimizing the distance over which low-voltage, high-current power must travel.

## Grid-to-GPU Conversion Chain

The full chain: nuclear/generation → hundreds-of-kV transmission → medium-voltage substation (10–30 kV AC) → utility room (430 V three-phase industrial) → rack PSU (48 V DC) → intermediate bus converters (12 V or 6 V) → voltage regulator modules (VRMs, 0.65–1.0 V at the GPU). Every stage uses distinct technologies and different vendor ecosystems — making power a "wide open" market with far more participants than the consolidated three-vendor HBM space.

## Topology Battle

Two competing approaches are forming: (1) incumbents favor 800V → 48V conversion, preserving existing 48V infrastructure; (2) challengers — notably TI and Navitas — advocate skipping 48V entirely and converting 800V directly to 6–12V, eliminating a conversion stage and improving end-to-end efficiency. No architecture is yet standardized.

## Coherent / InP Supply

Coherent CEO James Anderson cited aggressive six-inch InP wafer ramp: a 6-inch wafer yields >4× more die than a 3-inch wafer at <half the cost per die (area scales as r²: 36/9 = 4×; processing cost roughly 2× → 2× cost efficiency). Coherent is ramping six-inch capacity at **two sites in parallel** (including Järfälla, Sweden) and reports six-inch yields matching mature three-inch production across EMLs, CW lasers, and photodiodes. Vik flags key nuance: yield quality depends heavily on output power level (50 mW vs. 400 mW) and component complexity (EMLs are harder than CW lasers). The ultimate tell will be margins and ASPs — if high-power, high-ASP devices are selling at strong yields, it flows through to gross margin.

## Calls

- [[COHR]] — LONG — n/a — aggressive six-inch InP ramp at two sites with strong early yields positions Coherent to capture surging CPO laser demand at improving unit economics
- [[NVDA]] — MENTION — n/a — Rubin Ultra / Kyber rack roadmap is the demand driver for 800V power; NVIDIA itself is exploring 800V architectures
- [[TXN]] — MENTION — n/a — cited as a challenger promoting direct 800V-to-6V conversion, bypassing 48V incumbents
- [[NVTS]] — MENTION — n/a — cited alongside TI as advocating direct high-voltage-to-low-voltage conversion to eliminate intermediate bus stages
