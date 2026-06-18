---
type: source
title: "AMD vs NVIDIA Inference Benchmark: Who Wins? - Performance & Cost Per Million Tokens"
tags: []
related: []
created: 2025-05-23
updated: 2025-05-23
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/amd-vs-nvidia-inference-benchmark-who-wins-performance-cost-per-million-tokens"
venue: SemiAnalysis
post_date: 2025-05-23
tickers: [AMD, NVDA]
---

[[semianalysis]] publishes a comprehensive head-to-head inference benchmark pitting AMD's MI300X, MI325X, and MI355X against NVIDIA's H100, H200, and B200, across frameworks vLLM, SGLang, and TensorRT-LLM (TRT-LLM), evaluated on Llama 3 70B and 405B at varying latency targets.

**NVIDIA wins decisively in the rental market.** Over 100 Neocloud providers offer H200 rentals at roughly $2.50/hour, while only a handful list MI300X/MI325X — and at inflated prices above $2.50/hour. AMD would need MI300X rentals at ~$1.90/hour to be cost-competitive, and MI325X at $2.75–$3.00/hour depending on workload. At current market rates, NVIDIA wins on performance-per-dollar regardless of raw hardware capability.

**For owned hardware, AMD is occasionally competitive but not dominant.** The MI325X matches or beats the H200 on cost-per-million-tokens for large dense models (Llama 3 405B) at high concurrency, and generally offers lower hourly total cost of ownership. However, H200 with TRT-LLM delivers up to 1.5x throughput versus MI325X at equivalent latency constraints across most configurations. The B200, in preliminary testing, "crushes all other setups at every latency," further cementing NVIDIA's roadmap advantage.

**AMD's software ecosystem is the more damning problem.** SGLang's ROCm CI coverage is less than 10% of parity with NVIDIA. Roughly 25% of tested models fail accuracy benchmarks on ROCm — producing materially inferior outputs versus the same model on CUDA. AMD also lacks disaggregated prefill, Smart Routing, and NVMe KV cache tiering that NVIDIA's Dynamo framework provides, all of which matter for production inference deployments.

**Capital allocation signals misplaced priorities.** In Q1 2025, AMD spent approximately $749M on stock buybacks while allocating only ~$13M quarterly to internal R&D cluster infrastructure. The authors argue this constrains AMD's software development velocity at exactly the moment it needs to close the gap with NVIDIA's deeply integrated hardware-software stack.

**MI325X shipment delays compounded the problem.** Planned for Q3 2024, MI325X slipped to Q2 2025, prompting most hyperscalers to commit to NVIDIA B200 instead. AMD's window to capture the next datacenter cycle has narrowed significantly.

The conclusion is that NVIDIA's moat is primarily software and ecosystem, not raw silicon — but AMD has not invested enough to close that gap.

## Calls

- [[AMD]] — SHORT — n/a — Weak software ecosystem, inflated rental pricing, misallocated capex toward buybacks over R&D, and B200 displacement at hyperscalers make AMD a structurally disadvantaged inference competitor.
- [[NVDA]] — LONG — n/a — Dominant in rental market, superior TRT-LLM software stack, B200 crushing all benchmarks, and deep hyperscaler relationships reinforce NVIDIA's inference moat.
