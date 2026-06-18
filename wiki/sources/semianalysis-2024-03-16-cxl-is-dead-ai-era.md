---
type: source
title: "CXL Is Dead In The AI Era"
tags: []
related: []
created: 2024-03-16
updated: 2024-03-16
authors: [semianalysis]
year: 2024
url: "https://newsletter.semianalysis.com/p/cxl-is-dead-in-the-ai-era"
venue: SemiAnalysis
post_date: 2024-03-16
tickers: [NVDA, AMD, ALAB, MRVL]
---
[[semianalysis]] (Dylan Patel and Jeremie Eliahou Ontiveros) argues that CXL — Compute Express Link — has become irrelevant for AI workloads despite renewed industry buzz surrounding Astera Labs' IPO, and that forecasts of a $15 billion CXL market by 2028 are "outright ridiculous."

**CXL's original four use cases.** The authors acknowledge that CXL was designed around four legitimate premises: memory expansion, memory pooling, heterogeneous compute integration, and composable server architectures. Each makes theoretical sense in a general-purpose datacenter context. The problem is that none of these use cases maps well onto the GPU-centric, bandwidth-saturated AI training cluster.

**The beachfront problem.** The central technical argument is about chip I/O edge area — what the authors call "beachfront." High-performance chips dedicate their perimeter to the fastest possible signaling. NVIDIA's H100 devotes two entire sides of the die to HBM memory stacks, leaving very little beachfront for anything else. The H100 exposes only 16 PCIe lanes (64 GB/s) versus NVLink's 450 GB/s per direction. Choosing to allocate beachfront to PCIe SerDes — which CXL rides on — rather than to Ethernet-style SerDes is "making your chip roughly 3x worse" in raw I/O bandwidth efficiency.

**PCIe SerDes vs. Ethernet SerDes.** PCIe's bit-error-rate specification of <1e-12 is far tighter than Ethernet's 1e-4, which constrains PCIe's ability to use forward error correction (FEC) and forces conservative signal margins. Ethernet-style SerDes at 112G and 224G speeds, already used by NVIDIA and increasingly by the broader ecosystem, deliver superior bandwidth density for scale-out AI interconnects.

**NVIDIA dominance; AMD's structural weakness.** NVIDIA has no CXL support on its accelerators — it routes all high-bandwidth traffic through NVLink and its proprietary switch fabric. AMD's MI300X similarly lacks proper CXL exposure; the MI300A offers limited CXL but uses most of its beachfront on PCIe-style SerDes, yielding roughly one-third the I/O bandwidth of Ethernet alternatives. The authors predict AMD will need to move off PCIe-style SerDes in the MI400 generation to remain competitive.

**Google and Marvell.** Google is cited as using Ethernet-style SerDes for its ICI interconnect fabric and developing a custom CXL chip in collaboration with Marvell — a niche application that does not validate the broader CXL-for-AI thesis.

**Conclusion.** Cluster-scale AI interconnects will be dominated by proprietary protocols (NVLink) or standard Ethernet/InfiniBand, not CXL. Companies and investors banking on CXL as a mainstream AI infrastructure layer — including Astera Labs heading into its IPO — are working from a flawed premise.

## Calls

- [[NVDA]] — LONG — n/a — architectural choices (NVLink, Ethernet SerDes, beachfront discipline) validated as correct for AI era; CXL irrelevance entrenches NVIDIA's proprietary interconnect moat
- [[AMD]] — SHORT — n/a — MI300X lacks proper CXL and uses inferior PCIe SerDes, yielding ~3x worse I/O bandwidth than NVIDIA; must redesign interconnect strategy for MI400
- [[ALAB]] — SHORT — n/a — Astera Labs' IPO built around CXL infrastructure thesis the authors consider fundamentally flawed for AI workloads
- [[MRVL]] — MENTION — n/a — collaborating with Google on a custom CXL chip for a narrow niche application, not a broad AI validation
