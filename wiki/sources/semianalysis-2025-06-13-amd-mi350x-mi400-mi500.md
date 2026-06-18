---
type: source
title: "AMD Advancing AI: MI350X and MI400 UALoE72, MI500 UAL256"
tags: []
related: []
created: 2025-06-13
updated: 2025-06-13
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/amd-advancing-ai-mi350x-and-mi400-ualoe72-mi500-ual256"
venue: SemiAnalysis
post_date: 2025-06-13
tickers: [AMD, NVDA, AVGO, MRVL, AMZN, META, MSFT, ORCL]
---

[[semianalysis]] analyzes AMD's Advancing AI event, providing a detailed technical and competitive assessment of the MI350X/MI355X, MI400, and MI500 GPU roadmap, along with software progress and ecosystem strategy.

**MI355X vs Nvidia B200:** The MI355X delivers competitive TCO for small-to-medium LLM inference — roughly 33% lower than HGX B200 for self-owned clusters — thanks to larger HBM (288GB vs 180GB) and modestly better FP8/FP6 throughput. However, it cannot compete with the GB200 NVL72 due to a critical scale-up gap: MI355X achieves only an 8-GPU scale-up world size versus Nvidia's 72-GPU domain, making all-to-all collective operations ~18x slower. AMD's marketing of the 128-GPU rack as "rack scale" is called out as misleading.

**Architecture (CDNA4):** Built on TSMC N3P (vs N5 for MI300), with 185B transistors (+21%). The base active interposer die consolidates from four quadrants to two halves, eliminating one axis of 2.5D Infinity Fabric and removing two-hop latency for opposite-corner traffic. Die-to-die bisection bandwidth rises from 4.8 TB/s to 5.5 TB/s; scale-up speed improves 20%. MI350X is 1,000W air-cooled; MI355X is 1,400W with liquid cooling support, yet delivers under 10% theoretical performance uplift despite 40% more power.

**MI400 (H2 2026):** The first genuinely rack-scale AMD GPU, featuring 72 logical GPUs in the scale-up domain, potentially competitive with Nvidia's VR200 NVL144. The "UALink" interconnect is rebranded Infinity Fabric over Ethernet — not the authentic UALink protocol — and will use Broadcom Ethernet Tomahawk 6 switches after Marvell/Astera Labs UALink switch delays. MI400 adds 144 flexible I/O lanes supporting PCIe 6.0, 128G UALink, 212G Infinity Fabric over Ethernet, and others.

**MI500 (late 2027):** Targets 256 physical/logical chips, stepping ahead of Nvidia's projected VR300 at 144.

**Software (ROCm 7):** Claims 3.5x average inference throughput improvement over ROCm 6. Key weaknesses persist: RCCL is a fork of Nvidia NCCL and is recommended for a full rewrite; DeepEP and Mooncake are absent from open-source repos; TMA hardware, async features, and KVCache manager parity with Nvidia Dynamo are missing. PyTorch CI for MI355X initiated but no PRs merged yet.

**Hyperscaler traction:** AWS is the title sponsor and AMD's first serious large-scale GPU deployment; Oracle is deploying 30,000 MI355Xs; Meta is expanding from inference to training; x.AI is planning production inference; OpenAI is supportive. Microsoft is ordering low MI355 volumes but is positive on MI400. AMD is financially backstopping Neocloud partners — agreeing to lease back capacity or act as purchaser of last resort — partly enabled by Nvidia's DGX Lepton Marketplace commoditizing GPU compute and pushing Neoclouds toward vendor diversification.

**Engineering compensation:** AMD AI engineers have historically been underpaid relative to market; HR flagged the gap but management delayed action. Restructuring is now a stated priority, though implementation timeline remains uncertain.

## Calls

- [[AMD]] — LONG — px@n/a — gaining hyperscaler adoption, improving software, and rack-scale MI400 roadmap position it as credible Nvidia alternative at lower TCO
- [[NVDA]] — LONG — px@n/a — maintains dominant scale-up (72-GPU NVL72 vs AMD's 8-GPU) and software ecosystem advantages; MI355X cannot displace GB200 NVL72
- [[AVGO]] — MENTION — px@n/a — Broadcom Tomahawk 6 switches selected for MI400 scale-out fabric after UALink switch delays
- [[MRVL]] — MENTION — px@n/a — Marvell UALink switch delays contributed to AMD choosing Broadcom for MI400; Thor-2/3 NIC adoption also facing headwinds
- [[AMZN]] — MENTION — px@n/a — AWS is title sponsor and AMD's first large-scale GPU customer, signaling meaningful cloud diversification away from Nvidia
- [[META]] — MENTION — px@n/a — expanding AMD GPU usage from inference to training; PyTorch engineers collaborating on ROCm support
- [[MSFT]] — MENTION — px@n/a — ordering low MI355 volumes but positive on MI400; not yet a major AMD GPU buyer
- [[ORCL]] — MENTION — px@n/a — deploying 30,000 MI355Xs; committed to AMD NIC alongside Tensorwave
