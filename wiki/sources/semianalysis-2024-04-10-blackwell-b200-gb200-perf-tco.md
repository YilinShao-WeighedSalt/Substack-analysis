---
type: source
title: "Nvidia Blackwell Perf TCO Analysis - B100 vs B200 vs GB200NVL72"
tags: []
related: []
created: 2024-04-10
updated: 2024-04-10
authors: [semianalysis]
year: 2024
url: "https://newsletter.semianalysis.com/p/nvidia-blackwell-perf-tco-analysis"
venue: SemiAnalysis
post_date: 2024-04-10
tickers: [NVDA, AMD, INTC]
---

[[semianalysis]] conducts a rigorous technical and economic analysis of Nvidia's Blackwell GPU family (B100, B200, GB200NVL72) versus the Hopper generation, arguing that Nvidia's headline 30x performance claim is a best-case marketing figure, not representative of typical workloads. The true performance uplift for GB200 versus H200 under equalized conditions is closer to 8x at the low end, with a more realistic adjusted range near 18x — still substantial but far below the keynote number.

**Key technical findings:**

- Raw FLOP improvements on B100 are modest: ~77% FP16/BF16 gains on roughly 100% more silicon area, implying declining per-area efficiency. Only B200 and GB200 recover per-area performance. Memory bandwidth grows ~67% (H200: 4.8 TB/s → B100: 8.0 TB/s).
- GB200 achieves only ~47% improvement in TFLOPS-per-watt versus H100, which the authors view as unremarkable without the additional leverage from FP4 quantization.
- Nvidia's keynote benchmark stacked the deck by comparing GB200 at FP4 against H200/B200 at FP8, and selected a latency-constrained long-context workload (32k input / 1k output, 5s TTFT) that structurally disadvantages Hopper-era systems where tensor parallelism exceeds 8 GPUs.
- When parallelism crosses the 8-GPU NVLink boundary onto InfiniBand/Ethernet, H200 throughput drops ~23%; the GB200NVL72's larger NVLink domain avoids this cliff entirely.

**TCO and pricing dynamics:**

The piece argues the more important question is performance-per-TCO. Unlike H100 over A100 (where Nvidia took outsized margins on modest performance gains), Blackwell pricing is described as "very aggressive, perhaps even benevolent" because of mounting competitive pressure: large installed bases of H100/H200, AMD MI300X gaining traction, and Intel Gaudi 2/3. This marks a structural shift in Nvidia's pricing power as hyperscaler custom silicon matures.

**Competitive context:**

AMD MI300X, Intel Gaudi, and hyperscaler-internal accelerators are cited as credible alternatives that forced Nvidia's hand on pricing. The analysis anticipates workloads migrating toward >100B-parameter models where GB200NVL72's pooled NVLink bandwidth delivers the most differentiated advantage.

## Calls

- [[NVDA]] — LONG — n/a — Blackwell pricing is strategically aggressive to lock in share before competition matures; GB200NVL72 remains the clear performance leader for large-model inference despite inflated headline claims
- [[AMD]] — MENTION — n/a — MI300X cited as credible competitive pressure contributing to Nvidia's pricing restraint on Blackwell
- [[INTC]] — MENTION — n/a — Gaudi 2/3 mentioned alongside AMD as emerging challengers curbing Nvidia's generational margin expansion
