---
type: source
title: "Groq Inference Tokenomics: Speed, But At What Cost?"
tags: []
related: []
created: 2024-02-21
updated: 2024-02-21
authors: [semianalysis]
year: 2024
url: "https://newsletter.semianalysis.com/p/groq-inference-tokenomics-speed-but"
venue: SemiAnalysis
post_date: 2024-02-21
tickers: [NVDA, MRVL]
---

[[semianalysis]] examines whether Groq's headline-grabbing inference speed — up to 4x the throughput of competing services at under one-third the price — translates into sustainable unit economics, ultimately concluding that Groq is architecturally advantaged only in narrow latency scenarios while Nvidia retains overwhelming superiority for throughput-at-scale workloads.

**Architecture and performance.** Groq's Language Processing Unit (LPU) uses a VLIW deterministic architecture with ~725mm² die area on GlobalFoundries 14nm and 230MB on-chip SRAM, entirely avoiding external HBM. Deploying Mixtral requires 576 chips (8 racks × 9 servers × 8 chips each), versus a single H100 at low batch sizes or two H100s at large batches. The lack of HBM makes per-chip BOM low (wafer cost ~$6,000 vs. ~$16,000 for H100), but Groq pays a sizable chip margin to Marvell for ASIC services and the system itself demands 144 CPUs and 144TB RAM versus 2 CPUs for an 8-GPU Nvidia node — dramatically inflating infrastructure cost and power overhead.

**Latency vs. throughput split.** At batch size 3, Groq holds a genuine architectural edge for latency-sensitive workloads (autonomous agents, chain-of-thought, code generation) because current GPU-based low-latency APIs are uneconomical for Nvidia. However, at large batch sizes Nvidia achieves "order of magnitude better performance per dollar on a BOM basis," making Groq non-competitive architecturally for high-throughput workloads. The H100 achieves ~280 tokens/second/user and ~420 with speculative decoding; applying speculative decoding on mixture-of-experts models like Mixtral poses additional challenges for Groq.

**TCO and pricing sustainability.** Groq charges ~$0.27 per million tokens — matching competitors — despite significantly higher system-level costs. The article stresses that simplified silicon BOM analysis "isn't the right way to look at the business case" once system costs, margins, and power are included. Given Groq's limited funding history (last major round 2021, $50M SAFE note, currently fundraising), pricing may reflect subsidized market acquisition rather than a positive-TCO calculation.

**Competitive roadmap.** Groq's next-generation 4nm chip (expected ~H2 2025) could materially improve economics. Nvidia's B100 was expected within weeks of publication and was "far from a sitting duck." Groq's U.S.-based supply chain (fabrication and packaging fully domestic) is a differentiated advantage relative to Nvidia/AMD/Google relying on Taiwan and South Korea.

**Bottom line.** Groq wins on latency for small batch sizes but the economics look strained at scale. The true benchmark for any AI hardware platform is performance per total cost of ownership, and on that metric Groq's current generation does not challenge Nvidia for mainstream inference workloads.

## Calls

- [[NVDA]] — LONG — n/a — dominant throughput inference platform; order-of-magnitude better performance/dollar at large batch sizes; B100 roadmap reinforces competitive moat against LPU architectures
- [[MRVL]] — MENTION — n/a — supplies custom ASIC services to Groq and collects chip margin, making it a passive beneficiary regardless of Groq's end-market success
