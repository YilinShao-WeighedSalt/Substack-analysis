---
type: source
title: "InferenceMAX: Open Source Inference Benchmarking"
tags: []
related: []
created: 2025-10-09
updated: 2025-10-09
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/inferencemax-open-source-inference"
venue: SemiAnalysis
post_date: 2025-10-09
tickers: [NVDA, AMD]
---

[[semianalysis]] introduces InferenceMAX, an open-source automated benchmarking framework that reruns a comprehensive suite of LLM inference benchmarks nightly across hundreds of chips, addressing the core problem that point-in-time benchmarks go stale as inference software improves daily. The project is available at inferencemax.ai and backed by endorsements from Jensen Huang (NVIDIA), Lisa Su (AMD), Scott Guthrie (Microsoft), OpenAI Stargate, CoreWeave, and others.

**Benchmark methodology:** InferenceMAX tests three models — LLaMA 3.3 70B (dense enterprise proxy), DeepSeek R1 670B MoE (proxy for frontier closed models like GPT-4o/5), and GPT-OSS 120B MoE (proxy for GPT-5 mini). It sweeps three input/output length pairs (chat: 1k/1k; reasoning: 1k/8k; summarization: 8k/1k), multiple precisions (FP8, FP4, MX4), and varying concurrency levels to plot the full throughput-versus-latency Pareto frontier. GPUs covered: H100, H200, B200, GB200 NVL72, MI300X, MI325X, MI355X.

**Key findings from the October 7, 2025 snapshot:**
- GB200 NVL72 with TRT-LLM + Dynamo delivers the best TCO per million tokens at low interactivity (<30–90 tok/s/user) for DeepSeek R1, with up to 4x better TCO vs. single-node alternatives; at high interactivity, the B200 single-node wins.
- Multi-Token Prediction (MTP) on GB200 NVL72 delivers 2–3x throughput improvement at 70–140 tok/s/user for DeepSeek R1.
- AMD MI355X is competitive with B200 on GPT-OSS 120B FP4 summarization below 225 tok/s/user TCO-normalized, but lags on Llama 70B FP4 (AMD FP4 kernels need work) and significantly on DeepSeek 670B FP8 SGLang (40% higher latency than H200).
- B200 is ~20% more energy-efficient than MI355X measured in tokens/s per provisioned MW; both achieve ~3x generational improvement over their predecessors (B200 vs. H100, MI355X vs. MI300X).
- On FP8 DeepSeek, MI325X lags H200 on SGLang; AMD ROCm AITER optimizations still in progress.
- MI325X vLLM beats H200 on cost per million tokens for Llama 70B FP8 across all interactivity levels; H200 TRT-LLM closes the gap or leads for some configurations.

**Software recommendations:** SemiAnalysis urges NVIDIA to allocate more engineering resources to vLLM and SGLang (vs. concentrating on TRT-LLM), improve Blackwell QA, and reduce the number of manual flags needed for good performance. AMD is advised to reduce ROCm-specific flag requirements (work already underway) and prioritize FP4 kernel optimization.

**Roadmap:** Google TPU and AWS Trainium integration within two months; nightly evals (MATH-500, GPQA-Diamond) on FP4 models; disaggregated prefill + wide expert parallelism testing on MI300/MI355/B200; HGX B300 and GB300 NVL72 Blackwell Ultra benchmarks pending.

## Calls

- [[NVDA]] — LONG — n/a — GB200 NVL72 with TRT-LLM/Dynamo leads on TCO per token at scale and per-MW efficiency; MTP delivers 2–3x throughput gains; recommendation to invest more in open-source inference engines is constructive long-term.
- [[AMD]] — NEUTRAL — n/a — MI355X is TCO-competitive with B200 on some workloads (GPT-OSS 120B summarization) but lags on FP4 Llama and FP8 DeepSeek; ROCm software improving rapidly with AMD 2.0 urgency, but gap remains.
