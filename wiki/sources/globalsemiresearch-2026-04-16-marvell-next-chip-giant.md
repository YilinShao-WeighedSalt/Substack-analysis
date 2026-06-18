---
type: source
title: "Four Technologies Are Making Marvell the Next Chip Giant"
tags: []
related: []
created: 2026-04-16
updated: 2026-04-16
authors: [globalsemiresearch]
year: 2026
url: "https://globalsemiresearch.substack.com/p/four-technologies-are-making-marvell"
venue: Global Semi Research
post_date: 2026-04-16
tickers: [MRVL, NVDA, AVGO, AMD, INTC, GOOGL, AMZN, MSFT]
---

[[globalsemiresearch]] argues that Marvell is undergoing a strategic transformation from a network chip supplier into a full-stack AI data center company, positioning it to become the next chip giant after NVIDIA and Broadcom. The thesis rests on four interlocking technologies.

**UALink Switch.** The UALink 1.0 standard (released April 2025) is a coalition response to NVIDIA's proprietary NVLink, backed by AMD, Intel, Google, Microsoft, Meta, Broadcom, Cisco, AWS, Apple, and Alibaba Cloud. Marvell supplies custom UALink scale-up solutions using industry-leading 224G SerDes and physical-layer IP, and in January 2026 acquired XConn Technologies for $540 million — the maker of the Apollo hybrid CXL/PCIe switch — to strengthen its UALink switching capabilities and expand its engineering team. UALink is not expected to displace NVLink but will serve hyperscalers seeking to reduce NVIDIA dependency.

**CXL Chips (Structera Series).** With AI model memory requirements growing exponentially and HBM prices up over 200% in 2025-2026, Marvell's Structera line addresses the gap. The Structera X (DDR4/DDR5 memory expansion) is notably the industry's first CXL product supporting two CPUs simultaneously. The Structera A integrates 16 Arm Neoverse V2 cores with 4-channel DDR5 and a compression engine, delivering over 5x query-per-second improvement in vector search versus traditional CXL pooling. The Structera S 30260 (260-channel CXL 3.0 switch, built on XConn's Apollo technology) can share up to 48TB across 32 CPUs/GPUs at 4TB/s aggregate bandwidth, with sampling expected in Q3 2026. Structera has passed interoperability certification with AMD EPYC, Intel Xeon, and all three major DRAM vendors (Samsung, Micron, SK Hynix). Google and Meta compression specs are integrated, suggesting those hyperscalers are likely deployment partners.

**Google TPU ASIC (LPU).** Marvell has a substantial multi-year partnership to produce custom silicon for Google's proprietary AI accelerator platform — analogous to Broadcom's decade-long collaboration on Google TPUs. This represents a major anchor revenue stream.

**Proprietary Memory Architecture.** Marvell is developing a memory subsystem architectural innovation addressing memory access bottlenecks in AI systems; details remain limited in this post.

The author concludes that as compute bottlenecks shift toward memory and interconnect, Marvell's comprehensive stack — covering compute ASICs, memory expansion, and open-standard interconnects — combined with anchor partnerships at Google, AWS, and Microsoft, makes it a strong candidate to join NVIDIA and Broadcom as AI infrastructure giants.

## Calls

- [[MRVL]] — LONG — n/a — four-technology stack (UALink, CXL Structera, Google LPU ASIC, memory architecture) plus Google/AWS/Microsoft partnerships position Marvell to become the next AI chip giant
- [[NVDA]] — MENTION — n/a — dominant incumbent whose proprietary NVLink is the competitive foil; UALink coalition is an industry reaction against NVLink lock-in
- [[AVGO]] — MENTION — n/a — benchmark for ASIC partnership success via decade-long Google TPU collaboration; Marvell is following a similar playbook
- [[AMD]] — MENTION — n/a — UALink alliance member and NVLink alternative ecosystem participant
- [[INTC]] — MENTION — n/a — UALink alliance member
- [[GOOGL]] — MENTION — n/a — anchor customer for Marvell's custom LPU ASIC and likely CXL Structera deployment partner
- [[AMZN]] — MENTION — n/a — hyperscaler customer for UALink and CXL solutions (Trainium/Inferentia ecosystem)
- [[MSFT]] — MENTION — n/a — hyperscaler developing custom AI chips; UALink alliance member and potential Marvell customer
