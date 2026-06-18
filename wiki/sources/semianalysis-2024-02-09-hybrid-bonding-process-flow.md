---
type: source
title: "Hybrid Bonding Process Flow - Advanced Packaging Part 5"
tags: []
related: []
created: 2024-02-09
updated: 2024-02-09
authors: [semianalysis]
year: 2024
url: "https://newsletter.semianalysis.com/p/hybrid-bonding-process-flow-advanced"
venue: SemiAnalysis
post_date: 2024-02-09
tickers: [AMD, AMAT, ACMR, 8035.T, 6146.T, 522.HK]
---

[[semianalysis]] provides a detailed process-engineering breakdown of hybrid bonding — the bumpless, direct copper-to-copper interconnect technology that the authors call "the most transformative innovation to semiconductor manufacturing since EUV" — covering cleanroom requirements, surface preparation, TSV formation, CMP, and wafer-to-wafer (W2W) versus die-to-wafer (D2W) economic tradeoffs.

**Why hybrid bonding matters.** Conventional flip-chip packaging uses solder bumps with a practical pitch floor around 40–100µm. Hybrid bonding eliminates the bump entirely, achieving sub-10µm pitch and a path to sub-micron interconnect density. The result is dramatically lower resistance, higher bandwidth density, and smaller z-height — enabling true 3D die stacking in logic, memory, and image sensors.

**Process requirements.** The technology demands ISO 2–3 cleanroom standards — far more stringent than typical back-end packaging. A single 1µm particle creates a bond void ~10mm in diameter. Dielectric surface roughness must be held within 0.5nm and copper pad surfaces within 1nm, requiring multi-step CMP with tailored slurry chemistries to control copper dishing. Plasma dicing and laser dicing are preferred over blade dicing to minimize particulate generation. Before bonding, wafers undergo N₂ plasma activation to increase surface hydrophilicity, followed by DI water megasonic cleaning for final particle removal.

**TSV and hybrid bond layer formation.** A via-middle approach dominates TSV formation, using deep reactive ion etching (DRIE), CVD insulation/barrier deposition, PVD seed layer, and electrochemical copper fill followed by backside thinning. The hybrid bond layer itself uses PECVD SiCN dielectric, copper damascene plating, and multi-step CMP.

**W2W vs. D2W economics.** W2W delivers superior alignment accuracy (sub-50nm) and higher throughput but cannot accommodate known-good-die selection — making it economical only for smaller dies with high yields (CMOS image sensors, 3D NAND, Graphcore Bow IPU). D2W enables KGD sorting and is necessary for larger dies and heterogeneous integration; cost crossover occurs around mid-size die, with W2W costs escalating steeply as die area and scrap loss grow.

**Adoption landscape.** AMD's 3D V-Cache (2022) was the first major logic deployment. Sony, OmniVision, and Samsung lead in CMOS image sensors; YMTC, Western Digital, and Kioxia use it in 3D NAND. TSMC, Intel, SK Hynix, Micron, Bosch, and Adeia are cited as future participants. The equipment ecosystem spans BESI and SET for D2W bonding, EV Group (SmartView dual-camera alignment) for W2W, Applied Materials and Tokyo Electron for deposition and CMP, ASMPT for pick-and-place, DISCO for dicing, and ACM Research for megasonic cleaning.

## Calls

- [[AMD]] — MENTION — n/a — named as first major logic adopter of hybrid bonding via 3D V-Cache in 2022; substantive discussion of its role validating the technology for CPU/GPU stacking
- [[AMAT]] — MENTION — n/a — identified as key equipment supplier for hybrid bonding deposition and CMP process steps
- [[ACMR]] — MENTION — n/a — cited for megasonic cleaning tools used in pre-bond particle removal, a critical enabling step
- [[8035.T]] — MENTION — n/a — Tokyo Electron named as major process equipment supplier across deposition and CMP modules
- [[6146.T]] — MENTION — n/a — DISCO named for dicing and singulation equipment, where plasma/laser dicing is preferred over blade to control particulate contamination
- [[522.HK]] — MENTION — n/a — ASMPT cited for pick-and-place tooling in D2W bonding assembly
