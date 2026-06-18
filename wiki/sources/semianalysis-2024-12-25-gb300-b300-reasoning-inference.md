---
type: source
title: "Nvidia's Christmas Present: GB300 & B300 - Reasoning Inference, Amazon, Memory, Supply Chain"
tags: []
related: []
created: 2024-12-25
updated: 2024-12-25
authors: [semianalysis]
year: 2024
url: "https://newsletter.semianalysis.com/p/nvidias-christmas-present-gb300-b300-reasoning-inference-amazon-memory-supply-chain"
venue: SemiAnalysis
post_date: 2024-12-25
tickers: [NVDA, MU, MPWR, AMZN, MSFT]
---

[[semianalysis]] analyzes Nvidia's GB300 and B300 GPUs, released just six months after the GB200/B200 generation. The post argues these are more than incremental refreshes — they represent a deliberate architectural pivot toward long-context reasoning inference workloads, driven by the demands of models like OpenAI o3.

**Performance and Memory Upgrades.** The GB300 NVL72 configuration delivers roughly 50% higher FLOPS versus the B200 at the product level. Power budgets rise to 1.4 kW (GB300) and 1.2 kW (B300) from 1.2 kW and 1.0 kW previously. Memory upgrades to 12-Hi HBM3E, providing 288 GB capacity per GPU at 8 TB/s bandwidth. The NVL72 configuration allows 72 GPUs to share memory with ultra-low latency, which is critical for expanding KV-cache capacity during long-context reasoning chains. Historical benchmarks cited show the H100-to-H200 transition achieved 43% higher interactivity and approximately 3x cost reduction through better batch-sizing.

**Supply Chain Restructuring — Winners and Losers.** Nvidia is fundamentally changing how it ships hardware. Rather than supplying complete Bianca boards, it will deliver modular components: the B300 on an SXM Puck module, Grace CPU in BGA package, HMC from Axiado (replacing Aspeed), and LPCAMM modules from Micron replacing soldered LPDDR5X. This shift redistributes margin and manufacturing share significantly. Wistron loses Bianca board assembly share; Foxconn Industrial Internet (FII) gains as exclusive SXM Puck manufacturer. Micron benefits from memory module sourcing. Samsung is described as receiving "coal from Santa" — a nine-month exclusion window from key supply. Monolithic Power Systems (MPWR) is hurt as VRM components move to hyperscaler-direct procurement, with MPWR stock having fallen over 37% on this news.

**Hyperscaler Customization and Amazon.** The modular architecture allows hyperscalers to customize mainboards and cooling solutions at a level previously unavailable. Amazon specifically benefits: it can now deploy NVL72 with water-cooled components and deploy K2V6 400G NICs at scale in Q3 2025. Microsoft is flagged as a slower adopter, still purchasing some GB200 in Q4.

**Networking.** ConnectX-8 NICs provide twice the scale-out bandwidth versus ConnectX-7, with 48 PCIe lanes versus 32, enabling SpectrumX capability without requiring Bluefield 3 DPUs. This also enables air-cooled MGX B300A architectures.

**Nvidia Margin Dynamics.** As components shift from Nvidia's direct supply to ODM and hyperscaler procurement, margin structure changes — components are "pulled out of Nvidia's margin stacking, onto ODMs."

## Calls

- [[NVDA]] — LONG — n/a — GB300/B300 are purpose-built for reasoning inference demand, extending Nvidia's dominance into next-generation long-context workloads
- [[MU]] — LONG — n/a — Micron gains from LPCAMM module sourcing as Samsung is excluded for nine months
- [[MPWR]] — SHORT — n/a — VRM component procurement shifts directly to hyperscalers, removing Monolithic Power from Nvidia's margin stack; stock already down 37%+
- [[AMZN]] — LONG — n/a — Amazon is the primary hyperscaler beneficiary of the modular GB300 design, enabling NVL72 water-cooling and 400G NIC deployments
- [[MSFT]] — MENTION — n/a — Flagged as a slower GB300 adopter, still buying GB200 in Q4
