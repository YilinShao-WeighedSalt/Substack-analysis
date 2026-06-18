---
type: source
title: "The EDA Primer: From RTL to Silicon"
tags: []
related: []
created: 2026-05-12
updated: 2026-05-12
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/the-eda-primer-from-rtl-to-silicon"
venue: SemiAnalysis
post_date: 2026-05-12
tickers: [SNPS, CDNS, TER, AVGO, AMD, NVDA]
---

[[semianalysis]] (author Gerald Wong) presents Part 1 of a three-part EDA series, laying the technical groundwork of modern chip design and establishing why EDA software is indispensable infrastructure. The core tension is a widening design productivity gap: chip complexity is growing ~50% annually (AMD MI455X at 320 billion transistors) while engineering productivity improves only ~20% per year, creating compounding demand for EDA automation and a structural moat for the Big-3 vendors.

**The 13-stage design waterfall.** The post maps chip development from planning through production across five phases: (1) front-end design (RTL coding in SystemVerilog, UVM/formal verification, RTL freeze); (2) physical design (logic synthesis, placement, routing, clock tree synthesis); (3) signoff (DRC/LVS, timing closure via PrimeTime/Tempus, power integrity via RedHawk-SC/Voltus); (4) tapeout and fabrication (GDSII export, 8-12 week foundry runs); and (5) post-silicon validation (ATE testing, HTOL burn-in, speed binning). Verification alone consumes up to 70% of project effort and is the fastest-growing job category in chip development.

**Tool ownership is highly concentrated.** Synopsys and Cadence together handle "virtually every advanced-node chip taped out today" across synthesis (Design Compiler, Genus) and place-and-route (IC Compiler II, Innovus). Siemens EDA's Calibre is the dominant physical verification tool. Simulation is split among VCS (Synopsys), Xcelium (Cadence), and Questa (Siemens). Formal verification tools JasperGold (Cadence) and VC Formal (Synopsys) are critical for exhaustive property checking. Synopsys TCAD Sentaurus is highlighted as the key tool for foundry process simulation.

**PDK access tiers entrench anchor customers.** Process Design Kits mature through four stages (0.1→0.5→0.9→1.0). Tier 1 anchor customers — Apple, AMD, NVIDIA — receive PDKs 2-3 years before production, compounding their design advantage and deepening EDA vendor relationships. TSMC N2's FinFlex architecture (mixing cell heights like 3-2 or 2-1) is cited as a recent example of this co-optimization, with top-tier customers developing custom standard cell libraries yielding up to 15% PPA improvements.

**Post-silicon testing is an often-overlooked bottleneck.** Automatic Test Equipment from Teradyne and Advantest is required for every chip; HTOL burn-in typically runs 72-168 hours. Speed binning (harvesting chips at different frequency/voltage bins) is standard practice — NVIDIA GPUs routinely ship with defective SMs disabled. First silicon (A0) rarely reaches production; multiple steppings are budgeted, with full-mask respins costing tens of millions.

**Structural demand drivers are durable.** The engineering talent shortage (one-third of U.S. semiconductor workforce over age 55) and the 50%/20% complexity/productivity gap together ensure EDA tool demand is cycle-resistant. The post sets up Part 2 (market dynamics of the Big-3 vendors) and Part 3 (AI disruption potential via agentic design flows).

## Calls

- [[SNPS]] — MENTION — n/a — Dominant tool position across synthesis (Design Compiler/Fusion Compiler), signoff (PrimeTime), physical verification (IC Validator), TCAD (Sentaurus), and formal verification (VC Formal); foundational role at every advanced-node tapeout
- [[CDNS]] — MENTION — n/a — Broad coverage across simulation (Xcelium), place-and-route (Innovus), formal (JasperGold), timing (Tempus), power (Voltus), and emulation (Palladium); co-equal with Synopsys at advanced nodes
- [[TER]] — MENTION — n/a — Automatic Test Equipment supplier for post-silicon validation; every chip tapeout is a downstream ATE demand event
- [[AVGO]] — MENTION — n/a — Referenced implicitly through custom ASIC design complexity (multi-die chiplet architectures, STCO); Intel Ponte Vecchio (47 dies, 5 nodes) and AMD MI455X cited as drivers of EDA demand
- [[AMD]] — MENTION — n/a — MI455X (320B transistors) cited as the benchmark for accelerating design complexity driving EDA tool demand
- [[NVDA]] — MENTION — n/a — Tier 1 PDK anchor customer; GPU speed binning and SM disabling practices cited as standard post-silicon yield management
