---
type: source
title: "Scaling the Memory Wall: The Rise and Roadmap of HBM"
tags: []
related: []
created: 2025-08-12
updated: 2025-08-12
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/scaling-the-memory-wall-the-rise-and-roadmap-of-hbm"
venue: SemiAnalysis
post_date: 2025-08-12
tickers: [NVDA, MU, 000660.KS, 005930.KS]
---

[[semianalysis]] examines HBM's architecturally non-negotiable role in AI accelerators, tracing supply chain dynamics, manufacturing complexity, and the roadmap through HBM4E and beyond.

**Technology fundamentals.** HBM combines vertically stacked DRAM dies with ultra-wide data paths via Through-Silicon Vias (TSVs), delivering superior bandwidth and energy efficiency versus DDR or SRAM. TSV capacity is now the primary differentiating process step — and the binding production constraint. Manufacturing requires double-sided bumping, advanced packaging (CoWoS with interposers), and precise power-distribution-network (PDN) management across stacked layers. Stack yields degrade exponentially with layer count: an 8-layer stack at 99% per-layer yield produces ~92% good units; 12 layers drops to ~87%.

**Competitive landscape.** SK Hynix leads with MR-MUF molded underfill technology offering thermal advantages and a proprietary all-around power TSV design (6× higher TSV count, 75% lower VPP voltage drop). Micron entered with HBM3E claiming 30% lower power consumption — not yet independently verified. Samsung is positioned as the most aggressive technology promoter (loudest on hybrid bonding for HBM4) but continues a pattern of failing execution, with inferior yields relative to peers.

**Demand trajectory.** NVIDIA is the dominant HBM buyer through 2027; Google (TPU/MTIA) and Amazon (direct procurement) follow. Per-system HBM capacity scales explosively: A100 (80 GB HBM2E) → H100 (141 GB HBM3) → GB200 (192 GB HBM3E) → Rubin Ultra (1,024 GB HBM4E). The driver is LLM inference: workloads are memory-bandwidth-bound, extended context windows create exponential KV-cache capacity pressure, and "the Memory-Parkinson dynamic" ensures each generational capacity increase is immediately absorbed by larger models.

**Supply chain risk: Hanmi bonding tools.** In April 2025, SK Hynix ordered thermocompression bonders from Hanwha at a premium, bypassing Hanmi's near-monopoly. Hanmi retaliated by pulling field-service teams from SK Hynix fabs, threatening production continuity. SK Hynix subsequently placed a reconciliation order with Hanmi. The episode exposes the fragility of specialized TC-bonder supply — alignment requirements are sub-micron for 40 µm TSV pitches, with only a handful of qualified suppliers globally.

**HBM4 structural shift.** JEDEC relaxed the HBM4 stack-height standard from 720 µm to 775 µm, sidestepping bump-less hybrid bonding and its yield/cost risks. More importantly, HBM4 introduces custom base dies: accelerator makers (NVIDIA, AMD, OpenAI) will co-design logic dies optimized for their specific memory architectures rather than using generic foundations — a structural shift in memory–compute co-design philosophy.

**China.** CXMT is targeting HBM2 mass production in H1 2025 with TSV capacity matching Micron by year-end. Huawei affiliates XMC and SJSemi are at R&D scale, with a ramp-up planned. The article notes a reported $200 billion subsidy target for China's semiconductor development over five years.

## Calls

- [[NVDA]] — LONG — n/a — dominant HBM demand driver through 2027, scaling to 1 TB per system in Rubin Ultra; memory architecture shapes the entire HBM supply chain
- [[MU]] — LONG — n/a — credible HBM3E entrant with 30% lower power claim and growing share; beneficiary of HBM capacity constraints
- [[000660.KS]] — LONG — n/a — SK Hynix is the HBM technology and yield leader with MR-MUF and superior TSV design; best-positioned supplier through HBM4
- [[005930.KS]] — SHORT — n/a — Samsung lags on HBM yields and has a pattern of over-promising aggressive technology (hybrid bonding) while under-delivering execution
