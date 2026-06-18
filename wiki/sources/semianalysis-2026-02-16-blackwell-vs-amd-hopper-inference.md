---
type: source
title: "InferenceX v2: NVIDIA Blackwell Vs AMD vs Hopper - Formerly InferenceMAX"
tags: []
related: []
created: 2026-02-16
updated: 2026-02-16
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/inferencex-v2-nvidia-blackwell-vs"
venue: SemiAnalysis
post_date: 2026-02-16
tickers: [NVDA, AMD]
---

[[semianalysis]] publishes InferenceX v2 (formerly InferenceMAX), an open-source benchmark of nearly 1,000 frontier GPU configurations, revealing a decisive and widening performance gap favoring NVIDIA's Blackwell architecture over both AMD's MI355X and NVIDIA's prior Hopper generation.

**Blackwell performance leap exceeds expectations.** The GB300 NVL72 delivers up to 100x throughput improvement versus H100 on FP4 workloads (65x on FP8) at 75 tokens/second/user interactivity thresholds. Jensen Huang's GTC 2024 promise of 30x Blackwell uplift proved conservative — actual measured gains reached 98–100x in optimized disaggregated configurations. The B200 with TensorRT-LLM decisively outperforms AMD's MI355X in FP4 disaggregated prefill scenarios.

**NVL72 rack-scale bandwidth is the architectural moat.** NVLink provides 900 GB/s per GPU across 72 GPUs in the NVL72, versus 100 GB/s per GPU over InfiniBand XDR for multi-node B300 configurations — a 9x bandwidth advantage that directly translates to superior cost-per-token at high throughput.

**AMD is competitive only in constrained scenarios.** MI355X matches B200 performance in single-node FP8 disaggregated inference with SGLang, and offers competitive cost-per-token on that narrow basis. However, AMD's critical weakness is composability: when combining FP4 + disaggregated prefill + wide expert parallelism simultaneously (as real production deployments require), MI355X fails. MI355X still runs on forked vLLM 0.10.1 while official 0.15.1 crashes; vLLM CI contains zero MI355X test coverage; AMD's ATOM engine lacks disaggregated serving and wide expert parallelism; and there are zero production customers using ATOM. SemiAnalysis estimates AMD is 6+ months behind NVIDIA on distributed inference composability.

**Multi-Token Prediction (MTP) delivers dramatic economics.** DeepSeek R1 FP4 on GB300 with Dynamo TRT-LLM shows MTP reducing inference cost from $2.35/million tokens (without MTP at 150 tok/sec/user) to $0.11/million tokens — a ~21x reduction at equivalent interactivity. Real-world cloud pricing from Crusoe Energy implies ~83% gross margin potential at $0.226/M input tokens COGS.

**Software stack rankings:** TensorRT-LLM leads with mature disaggregated + wide expert parallelism support serving billions of tokens/hour globally. SGLang is competitive on FP8 B200. AMD's stack requires significant upstream engineering investment — SemiAnalysis recommends AMD redirect engineers from single-node projects to multi-node disaggregated inference.

## Calls

- [[NVDA]] — LONG — n/a — GB300 NVL72 delivers 100x inference throughput vs H100; Blackwell's architectural and software moat in disaggregated serving with wide expert parallelism is widening, not narrowing.
- [[AMD]] — SHORT — n/a — MI355X competitive only on single-node FP8; composability failures across FP4 + disaggregated + wide EP mean AMD has zero production inference customers and is 6+ months behind NVIDIA on the techniques that matter.
