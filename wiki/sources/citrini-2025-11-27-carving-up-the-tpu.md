---
type: source
title: "Carving Up the TPU"
tags: []
related: []
created: 2025-11-27
updated: 2025-11-27
authors: [citrini]
year: 2025
url: "https://www.citriniresearch.com/p/carving-up-the-tpu"
venue: Citrini Research
post_date: 2025-11-27
tickers: [GOOGL, NVDA, CRWV, META, WULF]
---

[[citrini]] argues that Google's TPU advantage is a structural, not merely technical, edge — and that the market's belated recognition of this thesis (first published in their August 2025 State of the Themes with an explicit "Long GOOGL" call) is both validating and a reason for caution about over-extrapolation.

The piece opens with a primer on TPU architecture. Unlike GPUs — which use thousands of generalized streaming multiprocessors — TPUs are built around systolic arrays of multiply-accumulate (MAC) cells that accept only data, not instructions. This eliminates instruction-level caches, maximizes utilization, and achieves high performance per watt on matrix multiplication workloads. The tradeoff is near-zero flexibility outside ML. Google's Gemini 3 demonstrates that frontier model training is achievable on TPUs, with an apparent energy-per-inference advantage over GPU-based rivals.

On NVDA, Citrini takes a deliberately non-sensationalist stance. CUDA/PyTorch switching costs remain high — TPU workflows require JAX, a non-trivial migration that took Google itself a decade to optimize. Despite the competitive framing, Google is still one of NVDA's largest customers. The post frames the Gemini 3 success as broadly bullish for compute demand: competing labs locked into NVDA will accelerate purchases of next-gen chips (Blackwell) to close the gap. The real margin risk for NVDA is medium-term (2027–2028), not near-term. Both Google and NVDA compete for the same CoWoS packaging capacity at TSMC, keeping the supply-chain bottleneck intact.

On TPU distribution strategy, Citrini argues Google has effectively already decided to sell TPUs externally. Evidence includes chip sales/deployments with Anthropic, Meta, and Fluidstack (via a $3.2B backstop with 14% equity in Terawulf-hosted capacity). Meta reportedly wants TPUs for training, not just inference. The "franchise model" — neocloud operators supply power and shells, Google drops in TPUs — is presented as a margin-accretive, capex-light path that also provides telemetry and locks in ecosystem presence before a Chinese competitor fills the gap.

The post is partially paywalled; the full supply-chain beneficiary list sits behind the paywall.

## Calls

- [[GOOGL]] — LONG — px@n/a — Largest Dynamic AI basket allocation; vertical TPU integration is a structural cost and performance advantage as AI moves to mass-production phase
- [[NVDA]] — NEUTRAL — px@n/a — Near-term demand intact (CUDA moat, supply bottlenecks); margin risk is real but medium-term, and Gemini success is net bullish for overall compute demand
- [[CRWV]] — MENTION — px@n/a — Named as a neocloud approached by Google to deploy TPUs under the franchise model
- [[META]] — MENTION — px@n/a — Reported buyer of Google TPUs for training workloads, pursuing silicon diversity despite owning MTIA
- [[WULF]] — MENTION — px@n/a — Hosts Fluidstack's Google TPU deployment in NYC data center under the franchise arrangement
