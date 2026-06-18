---
type: source
title: "Vera Rubin Extreme Co-Design: An Evolution from Grace Blackwell Oberon"
tags: []
related: []
created: 2026-02-25
updated: 2026-02-25
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/vera-rubin-extreme-co-design-an-evolution"
venue: SemiAnalysis
post_date: 2026-02-25
tickers: [NVDA, APH, MU, 000660.KS, 005930.KS, TSM, AMD]
---

[[semianalysis]] provides a deep technical teardown of Nvidia's Vera Rubin platform announced at CES 2026, characterizing it as "extreme co-design supremacy" across six integrated silicon products. The VR NVL72 rack doubles performance and power density versus Blackwell while introducing sweeping manufacturability and thermal efficiency improvements.

## Six Silicon Products

The Rubin GPU moves to 3nm with 224 SMs (up from 160), delivering 35 PFLOPS dense FP4 (50 PFLOPS with adaptive compression, though many ML engineers remain skeptical of real-world attainability). Memory bandwidth nearly triples to 22 TB/s using HBM4 at 10.8 GT/s; initial shipments likely target ~20 TB/s due to supplier qualification gaps. TDP reaches 2,300W and transistor count hits 336 billion. The Vera CPU (codenamed Olympus) is an ARM-based 3nm design with 88 cores, 162 MB L3 cache, and 2.5x memory bandwidth increase via SOCAMM modules.

The NVLink 6 Switch doubles rack-level bandwidth via bidirectional 400G SerDes, with VR NVL72 containing 36 switches versus 18 in GB200. ConnectX-9 NICs offer dual 800G Ethernet. BlueField-4 co-packages a full Grace CPU die with ConnectX-9 and serves as the anchor for a new Context Memory Storage (CMX/ICMS) KV-cache fabric. Spectrum-6 doubles radix versus Spectrum-5 with 102.4T switching bandwidth, available in CPO and non-CPO configurations.

## Cableless Compute Tray and PCB Upgrades

The headline mechanical innovation reduces assembly time from 2 hours to 5 minutes by eliminating internal flyover cables entirely — signals now traverse a PCB midplane via board-to-board connectors. PCB area increases approximately 2.3x, and materials upgrade from M7 to M8/M9 class CCL with HVLP4 copper foil to maintain signal integrity across ~500mm PCIe Gen6 runs. Quartz cloth adoption remains under debate due to yield and cost challenges. Amphenol's PaladinHD2 connectors are the named midplane solution.

## Thermal and Power

Vera Rubin achieves 100% liquid cooling (versus 85% for Blackwell) with 100-micron micro-channels (down from 150-micron) and gold-plated cold plates to resist corrosion from indium liquid metal TIM2. Total rack TDP reaches 180–220 kW versus 120–140 kW for GB200. Power shelves deliver 415–480 VAC to 50 VDC via four 110 kW shelves; liquid-cooled busbars handle 5,000+ A. Hyperscalers increasingly adopt 800 VDC HVDC racks, eliminating mechanical chillers in favor of dry coolers and adiabatic towers.

## HBM and Supply Chain Winners/Losers

SK Hynix leads HBM4 qualification; Samsung is challenged on spec; Micron is "effectively out of the picture for Rubin HBM4" due to qualification gaps. Among component suppliers, Amphenol is a clear winner (connector volumes plus PCB area increase), as are cooling quick-disconnect vendors (Colder Products, Danfoss, Stäubli, Parker Hannifin) given 2–2.5x flow requirements. Mechanical chillers and traditional air-cooling infrastructure face structural demand reduction from the fully liquid-cooled design. The article warns that SSD volumes for the ICMS KV-cache fabric are "overblown by the industry."

## Calls

- [[NVDA]] — LONG — n/a — sole supplier of a fully integrated rack platform (GPU, CPU, switch, NIC, DPU, networking) with widening co-design lead over AMD and hyperscaler ASICs
- [[APH]] — LONG — n/a — Amphenol PaladinHD2 connectors displace internal cables; PCB area grows 2.3x, driving connector and substrate content sharply higher
- [[MU]] — SHORT — n/a — effectively disqualified from Rubin HBM4 supply due to qualification gaps, ceding share to SK Hynix and Samsung
- [[000660.KS]] — LONG — n/a — SK Hynix leads HBM4 ramp and is best positioned to capture outsized Rubin memory share
- [[005930.KS]] — MENTION — n/a — Samsung faces spec challenges on HBM4 but remains in the qualification race
- [[TSM]] — MENTION — n/a — sole 3nm foundry for Rubin GPU and Vera CPU; all six silicon products concentrated at TSMC
- [[AMD]] — MENTION — n/a — MI450X Helios cited as primary competitive reference; Nvidia's multi-product co-design advantage widens the gap
