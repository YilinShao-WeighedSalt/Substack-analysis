---
type: source
title: "TPUv7: Google Takes a Swing at the King"
tags: []
related: []
created: 2025-11-28
updated: 2025-11-28
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/tpuv7-google-takes-a-swing-at-the"
venue: SemiAnalysis
post_date: 2025-11-28
tickers: [NVDA, AVGO, GOOGL]
---

[[semianalysis]] delivers a comprehensive technical and commercial teardown of Google's TPUv7 Ironwood, arguing it is a credible challenger to Nvidia's GPU dominance in AI infrastructure and that its total cost of ownership (TCO) advantage is now large enough to reshape hyperscaler and neocloud procurement.

## Technical Architecture

TPUv7 Ironwood ships with 8-Hi HBM3E (192 GB capacity, matching GB200), a 256×256 systolic array (doubled from TPUv5p's 128×128), and is manufactured on TSMC N5 — the same node as TPUv6. Memory bandwidth is slightly below GB300, but the interconnect architecture is the key differentiator: a 3D torus ICI fabric with 1.5 optical transceivers per TPU at 800G, fed by 48 144×144 optical circuit switches (OCS), enabling clusters of up to 9,216 TPUs in a single pod and 147,000 TPUs at the datacenter network level. By comparison, typical GPU clusters max out at 64–72 nodes before requiring costly external networking.

## TCO Advantage

The article's central quantitative claim: Ironwood delivers ~44% lower TCO than Nvidia GB200 at Google's internal procurement costs, and ~30% lower TCO when sold externally via GCP despite Google's margin markup. At the workload level, if Anthropic achieves 40% model FLOP utilization (MFU) on TPUs, the effective TCO per PFLOP falls ~52% versus GB300.

## Commercial Traction and Customer Commitments

Anthropic has committed to over 1 million TPUs: ~400,000 TPUv7 Ironwoods purchased directly via Broadcom (~$10 billion silicon cost), plus ~600,000 units rented through GCP (~$42 billion in estimated revenue/RPO). Meta is identified as another major TPU customer. xAI, OpenAI, and SSI are named as pipeline customers; OpenAI has not yet deployed TPUs but is said to have already modeled ~30% savings versus its Nvidia fleet. Gemini 3 and Claude 4.5 Opus are noted as having been trained entirely on TPUs, representing state-of-the-art model quality.

## Software Ecosystem Progress and Gaps

Google is closing its historically weak software story: native PyTorch support is in development (moving away from lazy XLA graph capture), and the company contributed 1,400+ commits to vLLM and SGLang in 2025, plus specialized Pallas kernels achieving 3–4× speedup on paged attention and MoE workloads. Critical gap: XLA:TPU compiler, runtime, and MegaScale multi-pod training code remain closed-source, constraining ecosystem breadth compared to CUDA.

## Nvidia's Structural Risk

The article frames TPUv7 as the first credible proof that a non-Nvidia stack can deliver lower TCO at scale for frontier training and inference. The combination of Broadcom-manufactured silicon, Google's OCS fabric, and a software catch-up trajectory poses a genuine long-cycle demand headwind for Nvidia, particularly at hyperscaler and large neocloud accounts.

## Calls

- [[NVDA]] — SHORT — n/a — TPUv7 delivers materially lower TCO at scale for frontier AI workloads, threatening Nvidia's dominant share at hyperscaler and large neocloud accounts over a multi-year horizon
- [[AVGO]] — LONG — n/a — Broadcom manufactures TPUv7 silicon and benefits directly from Anthropic's ~$10 billion direct TPU purchase and Google's expanding custom ASIC program
- [[GOOGL]] — LONG — n/a — TPUv7's TCO advantage enables Google Cloud to offer superior AI economics versus commodity GPU clouds, strengthening GCP competitive positioning and locking in major AI lab customers via long-term RPO commitments
