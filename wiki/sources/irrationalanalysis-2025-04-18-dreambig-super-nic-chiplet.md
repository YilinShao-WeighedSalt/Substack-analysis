---
type: source
title: "DreamBig Semi: Crazy Super-NIC and Chiplet Hub"
tags: []
related: []
created: 2025-04-18
updated: 2025-04-18
authors: [irrationalanalysis]
year: 2025
url: "https://irrationalanalysis.substack.com/p/dreambig-semi-crazy-super-nic-and"
venue: Irrational Analysis
post_date: 2025-04-18
tickers: [NVDA]
---

[[irrationalanalysis]] profiles DreamBig Semiconductor, a private fabless startup founded by Weili Dai and Sehat Sutardja (former Marvell co-founders) alongside a large contingent of ex-Intel Mount Evans engineers. The author met with CEO Sohail and a DreamBig investor; he holds no economic interest in the company.

**Core technology: RDMA engine and Demios chiplet hub.** DreamBig's central IP is a high-performance RDMA (Remote Direct Memory Access) engine called Ares, which bypasses the CPU to process AI networking traffic. The company claims it processes more millions-of-packets-per-second (Mpps) than NVDA's ConnectX, noting that Nvidia has stopped publishing Mpps benchmarks. Their 800G NIC product (Mercury) is monolithic and relies on this digital IP.

**Demios chiplet hub.** The more ambitious product is the Demios Chiplet Hub — a UCIe-PHY-ringed die with 3D-stacked HBM acting as a packet buffer cache. By chaining Demios hubs, DreamBig can compose heterogeneous topologies mixing CPU, AI ASIC, and sensor chiplets. The HBM cache eliminates the packet-buffer bottleneck that limits conventional NICs, giving DreamBig a claimed performance and cost advantage over NVDA ConnectX 8.

**Silicon Box packaging risk.** Advanced packaging is critical to the Demios roadmap and is outsourced to Silicon Box, a related-party startup co-founded by the same Marvell duo. Silicon Box uses proprietary panel-level packaging technology; its feasibility at commercial yields is the author's biggest concern. If Silicon Box fails, DreamBig can fall back to TSMC CoWoS-S, which is viable for the two-chiplet Mercury NIC but would substantially compress gross margins on Demios-based products.

**Lead customer and validation.** DreamBig's lead customer is Mercedes-Benz (automotive/heterogeneous chiplet use case), providing NRE revenue and real-world packaging and traffic-pattern learning. The author views this as meaningful validation of the platform. The author identifies a low-probability (<1%) risk that a UCIe advanced-package PHY bug could require a ~6-month re-spin, but views DreamBig as investable even in a Silicon Box failure scenario.

**Conclusion.** The author is broadly constructive: the team has the pedigree to execute on Mercury, and the Demios chiplet hub is genuinely differentiated if Silicon Box delivers. Recommends the company to semiconductor partners and private-market investors seeking high-gross-margin semiconductor exposure.

## Calls

- [[NVDA]] — MENTION — n/a — Referenced as incumbent AI NIC vendor (ConnectX); DreamBig claims superior Mpps and cost vs. ConnectX 8, and notes Nvidia has stopped publishing Mpps benchmarks.
