---
type: source
title: "The Great AI Silicon Shortage"
tags: []
related: []
created: 2026-03-12
updated: 2026-03-12
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/the-great-ai-silicon-shortage"
venue: SemiAnalysis
post_date: 2026-03-12
tickers: [TSM, NVDA, AMD, MU, 000660.KS, 005930.KS, INTC, AVGO, AMKR]
---

[[semianalysis]] argues that AI infrastructure faces a multi-layer silicon crisis — logic wafers, memory, and advanced packaging — severe enough to cap compute deployment through at least 2027, with no near-term relief given fab construction timelines.

## Logic: TSMC N3 Wafer Crunch

Every major AI accelerator family converges on TSMC's N3 node in 2026: NVIDIA Rubin (N3P), Google TPU v7 (N3E), AMD MI350X/MI400 tiles (N3), AWS Trainium3 (N3P), and Meta MTIA. Networking silicon (NVLink 6 switches, Broadcom Tomahawk 6, Spectrum 6) and VR-rack CPUs follow. The result: AI is projected to consume 60% of N3 output in 2026 and 86% by 2027, crowding out smartphones and CPUs almost entirely. TSMC utilization is modeled to breach 100% in 2H 2026. Even if smartphone demand softens and 5–25% of those N3 wafers are reallocated, the gain is modest — 0.1–0.7 million incremental Rubin GPUs or 0.3–1.5 million additional TPU v7s.

## Memory: HBM and DRAM Squeeze

HBM consumes roughly 3× the wafer capacity of commodity DRAM per bit, widening to ~4× with HBM4. NVIDIA's Rubin raises HBM capacity 50% over Blackwell; Rubin Ultra drives a 4× increase. Customer demand for ~11 Gb/s HBM4 pin speeds is hard to meet at scale — SK Hynix and Samsung are ahead of Micron here. Meanwhile, VR NVL72 racks carry 3× more DDR content than Grace-based predecessors (1,536 GB vs. 512 GB per CPU). DDR margins have surged to near-HBM levels, removing memory suppliers' prior incentive to prioritize HBM expansion; future HBM capacity may require higher customer prices. A 25% decline in consumer device shipments would free only ~7% of total DRAM supply — enough to cover ~80% of annual HBM demand.

## Packaging: CoWoS Easing

CoWoS constraints are described as easing relative to logic shortages. TSMC is calibrating CoWoS investment to N3 wafer availability rather than overbuilding. OSATs (ASE/SPIL, Amkor) and Intel's EMIB provide incremental mitigation.

## Hyperscaler and Foundry Implications

Google's 2026 capex roughly doubled year-over-year for datacenters and servers. Hyperscalers report capacity hunger exceeding supply. Scarce TSMC N3 allocation is pushing customers toward Intel Foundry (backed by U.S. government support) and Samsung Foundry — Samsung has secured Tesla AI5/AI6 programs (dual-tracked with TSMC) and entered NVIDIA's datacenter supply chain. As a demand proof-point, Anthropic added $6B of ARR in February 2026 alone from Claude Code adoption, and would have added more with additional compute.

## Calls

- [[TSM]] — LONG — n/a — sole N3 supplier running above 100% utilization; pricing power and allocation control strengthen through 2027
- [[NVDA]] — LONG — n/a — demand massively exceeds supply for Rubin/Blackwell; silicon scarcity makes each GPU more valuable, not less
- [[AMD]] — MENTION — n/a — MI350X/MI400 on N3 competes for same scarce wafer pool, allocation outcome uncertain
- [[MU]] — NEUTRAL — n/a — behind SK Hynix and Samsung on HBM4 pin speeds; risks losing HBM share even as DRAM margins improve
- [[000660.KS]] — LONG — n/a — SK Hynix leads on HBM4 ramp; best positioned among memory suppliers
- [[005930.KS]] — LONG — n/a — Samsung gains foundry wins (Tesla, NVIDIA datacenter) as TSMC N3 allocation tightens
- [[INTC]] — MENTION — n/a — Intel Foundry benefits from overflow demand and U.S. government backing as TSMC alternative
- [[AVGO]] — MENTION — n/a — Tomahawk 6 and Spectrum 6 networking silicon compete for N3 wafers alongside AI accelerators
- [[AMKR]] — MENTION — n/a — Amkor cited as CoWoS-alternative OSAT providing packaging capacity relief
