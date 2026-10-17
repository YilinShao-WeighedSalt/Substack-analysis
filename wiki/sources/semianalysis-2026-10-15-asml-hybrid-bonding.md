---
type: source
title: "ASML Is Building a Hybrid Bonding Tool!"
tags: [hybrid-bonding, advanced-packaging, semiconductor-equipment, D2W]
related: ["[[semianalysis]]", "[[ASML]]", "[[BESI]]", "[[AMAT]]", "[[TSM]]", "[[INTC]]", "[[advanced-packaging]]", "[[semiconductor-equipment]]"]
created: 2026-10-17
updated: 2026-10-17
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/asml-is-building-a-hybrid-bonding"
venue: SemiAnalysis
post_date: 2026-10-15
tickers: [ASML, BESI, AMAT, TSM, INTC]
---

SemiAnalysis argues from patent filings, a March *The Elec* report, and ASML's own 2024 Investor Day roadmap that **ASML is building a die-to-wafer (D2W) hybrid bonding tool** — and likely a W2W tool on TWINSCAN too. SA calls hybrid bonding "the most transformative innovation in semiconductor manufacturing since EUV."

**Why it matters / why D2W:** W2W HB already runs in volume (image sensors, 3D NAND; DRAM next). D2W is slower — the industry lacks tools combining alignment accuracy and throughput (SA's check: upper bound ~1 wafer/hr), keeping cost/die high. D2W runs in volume only in **logic** today: AMD's hybrid-bonded V-Cache since 2022, TSMC SoIC at ~6µm pitch (→4.5µm ~2029). **Besi is the only supplier with D2W tools in volume**; everyone else is still qualifying a first tool.

**The tool (patent WO2025201788A1):** unlike a Besi-type bond head picking dies off a diced wafer, ASML moves single dies on independent holders around a **track** (names SuperTrak CONVEYANCE). Each die stops at inspection → cleaning → plasma activation → topography → leveling → coarse/fine alignment → bonding; the station's head moves to the die, not the reverse. Three benefits: independent shuttles keep every station busy ("occupy all process stations simultaneously"); add capacity by adding a station, not a second tool; heterogeneous integration = a new die type is just a new recipe.

**ASML's claimed edge:** the two factors setting bond yield are **alignment accuracy** and **particle control** — exactly what ASML has fought in litho for decades. It can reuse its ORION wafer-alignment sensor (reads a diffraction grating on each die through CMP/plasma-induced asymmetry); NXT:2100i holds 0.9nm overlay, and ASML already corrects post-bond overlay from 40-60nm to <4nm — an order of magnitude below the ~50nm a bonder needs. EUV-grade cleanliness ≥ a bonder's requirement (a single 1µm particle unbonds ~10mm). Prodrive (EUV maglev motors) + VDL ETG (frames) are the likely component suppliers.

**Vertical-integration context:** continuation of Cymer (2013), HMI (2016), Berliner Glas (2020); first back-end product XT:260 i-line packaging scanner shipped 3Q25; just announced a joint 6"→12" photomask initiative with TSMC/Intel/Samsung. The bonder can hand the scanner a die-position "coordinate system" so litho on bonded wafers is faster — ASML sells bonder + scanner as a pair, at a premium.

**Open challenges (post-paywall):** feed-forward metrology, the die-to-wafer contact, modifying non-bonding stations to process dies on the track, and keeping the whole loop clean (bonder contaminants = dicing debris + particles on activated hydrophilic surfaces, different from scanner contaminants).

## Calls
- **[[ASML]] — LONG (implied).** New back-end TAM; vertical-integration + litho-alignment/particle-control edge; prices at a premium; sells bonder+scanner as a pair. Logic (TSMC/Intel) adopts first.
- **[[BESI]] — SHORT (implied).** "Bad news for Besi." Logic is most of Besi's HB business (concentrated at TSMC/Intel, ASML's 20-yr customers). Besi's HBM prospects also weakening — HBM D2W adoption SA sees slipping to **2029 or beyond, if at all**; Korean challengers catching up.
- **[[AMAT]] — context.** Applied owns 9% of Besi and co-launched Kinex (integrated D2W bonder) with it last Oct — so ASML lines up against Applied here too.
