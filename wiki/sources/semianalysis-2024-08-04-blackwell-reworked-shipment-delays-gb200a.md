---
type: source
title: "Nvidia's Blackwell Reworked - Shipment Delays & GB200A Reworked Platforms"
tags: []
related: []
created: 2024-08-04
updated: 2024-08-04
authors: [semianalysis]
year: 2024
url: "https://newsletter.semianalysis.com/p/nvidias-blackwell-reworked-shipment"
venue: SemiAnalysis
post_date: 2024-08-04
tickers: [NVDA, TSM]
---
[[semianalysis]] reports that Nvidia's Blackwell family is encountering major production issues that have materially pushed out Q3/Q4 2024 and H1 2025 shipment targets. The root cause is twofold: (1) a design defect in the Blackwell package tied to TSMC's CoWoS-L technology, and (2) insufficient CoWoS-L capacity at TSMC.

CoWoS-L replaces CoWoS-S for future AI accelerators because silicon interposers hit a practical size limit (~3.5x reticle for AMD's MI300). CoWoS-L uses an organic RDL interposer with embedded silicon bridge dies to achieve higher I/O density. The aggressive ramp to over one million chips per quarter exposed a coefficient of thermal expansion (CTE) mismatch between the bridge dies and organic interposer, causing warpage. The bridges connecting the two main Blackwell compute dies — critical for the 10 TB/s chip-to-chip interconnect — require a redesign, along with rework of top-level metal routing and bump-out on the Blackwell die. This is identified as the primary cause of the multi-month delay.

TSMC is simultaneously converting existing CoWoS-S capacity at AP3 and building a new CoWoS-L fab (AP6), making the ramp lumpy. As a result, Nvidia is concentrating scarce CoWoS-L supply almost entirely on GB200 NVL72/NVL36x2 rack-scale systems, effectively cancelling the HGX B100 and B200 outside minimal initial volumes.

To fill demand in the interim, Nvidia is introducing the B200A based on a new single-die B102 chip with 4 stacks of HBM3E (up to 144 GB, up to 4 TB/s bandwidth). Because B102 is monolithic it can be packaged on CoWoS-S or alternative 2.5D suppliers (Amkor, ASE SPIL, Samsung). This allows Nvidia to serve lower/mid-tier AI demand without depending on CoWoS-L. The new MGX GB200A NVL36 is a fully air-cooled 40 kW/rack system with 36 GPUs and ConnectX-8 NICs, designed for datacenters unable to support liquid cooling. A cancelled NVL64 design was found thermally infeasible and networking-inefficient.

Supply chain impacts are broad: cooling, PCB, CCL, substrate, NVLink backplane copper content, active copper cable content, optics, BMC, and power delivery all shift. OEMs and ODMs face revenue/shipment schedule disruptions from 3Q 2024 through 2Q 2025. Hopper (H100/H200) gets an extended lifespan and higher-than-planned shipment volumes to compensate.

## Calls

- [[NVDA]] — MENTION — n/a — Blackwell production delayed by CoWoS-L packaging defects; product line reworked with new B200A/GB200A NVL36, Hopper extended; revenue and volume impact in 2H 2024–H1 2025
- [[TSM]] — MENTION — n/a — CoWoS-L capacity ramp is a bottleneck; bridge-die redesign and lumpy AP3/AP6 conversion are gating Blackwell supply
