---
type: source
title: "The New AI Networks | Ultra Ethernet UEC | UALink vs Broadcom Scale Up Ethernet SUE"
tags: []
related: []
created: 2025-06-11
updated: 2025-06-11
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/the-new-ai-networks-ultra-ethernet-uec-ualink-vs-broadcom-scale-up-ethernet-sue"
venue: SemiAnalysis
post_date: 2025-06-11
tickers: [AVGO, NVDA, AMD, AMZN]
---

[[semianalysis]] examines three competing standards for AI datacenter networking: Ultra Ethernet Consortium (UEC), UALink, and Broadcom's Scale Up Ethernet (SUE). The June 2025 release of the 565-page UEC specification marks a significant milestone in the industry's effort to displace proprietary interconnects with open Ethernet-based solutions.

**Ultra Ethernet Consortium (UEC)** targets scale-out networking across large multi-switch clusters, supporting tens of thousands of endpoints. Its specification standardizes the LibFabric API across NCCL, RCCL, MPI, and SHMEM protocols, targets round-trip latencies of 1–20 microseconds, and introduces "packet spraying" — entropy-based routing across multiple simultaneous paths to maximize bandwidth utilization. UEC deprecates legacy protocols (RoCE, DCQCN, PFC between switches) in favor of receiver-driven congestion control with sub-500ns accuracy. Packet trimming with tombstone headers handles severe congestion. UEC operates under the Linux Joint Development Foundation as a Standards Development Organization, with AMD prominently among its backers.

**UALink and Broadcom SUE** are narrower scale-up standards targeting single-switch domains of up to 1,024 endpoints. Both support 200GbE lane speeds (vs. UEC's 100GbE, noted as outdated) and memory-mapped interfaces. SUE's specification is only ~20 pages and delegates load balancing and packet spraying to software, keeping hardware complexity minimal. UALink uses credit-based flow control; SUE recommends PFC/CBFC. Both are positioned for intra-pod GPU-to-GPU communication rather than full cluster networking.

**Market context:** Standard Ethernet has been recovering market share from Nvidia InfiniBand through lower cost and greater customization. Hyperscalers including Amazon, Google, Meta, and Oracle have deployed Ethernet-based AI networks that now approach Nvidia InfiniBand performance. Crucially, Nvidia's Spectrum-X Ethernet now outships its Quantum InfiniBand in the Blackwell generation, validating the industry-wide shift to Ethernet for AI networking. All three standards anticipate NICs evolving into coprocessor IP blocks or chiplets integrated directly on host silicon, reducing footprint and latency.

**UEC challenges:** Plugin support for Amazon EFA is noted as not straightforward; multi-vendor interoperability ("plugfests") remains complex given specification depth; and performance on non-UEC networks requires additional validation work.

## Calls

- [[AVGO]] — MENTION — px@n/a — Broadcom authored the SUE standard, positioning its networking silicon for AI scale-up deployments
- [[NVDA]] — MENTION — px@n/a — Spectrum-X Ethernet outshipping Quantum InfiniBand in Blackwell signals Nvidia's own pivot toward Ethernet AI networking
- [[AMD]] — MENTION — px@n/a — AMD visibly backs the UEC standard, supporting open Ethernet alternatives to Nvidia's proprietary InfiniBand ecosystem
- [[AMZN]] — MENTION — px@n/a — Amazon EFA integration challenges highlight hyperscaler friction with UEC adoption despite deploying Ethernet-based AI clusters
