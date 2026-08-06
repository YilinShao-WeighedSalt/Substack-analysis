---
type: source
title: "Kimi K3, The Manos, The Mythos, The Legendos"
tags: [ai-models, inference-economics, attention-architecture, educational]
related: ["[[semianalysis]]", "[[ai-software-models]]", "[[NVDA]]", "[[AMD]]"]
created: 2026-08-06
updated: 2026-08-06
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/kimi-k3-the-manos-the-mythos-the"
venue: SemiAnalysis
post_date: 2026-08-03
tickers: []
---

# Kimi K3, The Manos, The Mythos, The Legendos

Architecture primer on **Kimi K3** (Moonshot AI), the open frontier model that swept leaderboards. **Educational — no equity call.** Relevant to inference-cost economics and the custom-silicon / serving-throughput backdrop.

## Key concepts

- **Kimi Delta Attention (KDA):** the linear-attention layer in K3's *hybrid* attention. Lineage: linear attention (drop softmax → O(Ld²), compress all past keys/values into one hidden state S) → DeltaNet (L2-norm delta rule regularizes S growth) → Gated DeltaNet (LSTM forget gate on S) → KDA (forget gate becomes a diagonal matrix for per-channel decay + positional awareness). Point: compress long context into a fixed-size memory state → cheaper serving than full softmax attention.
- **FlashKDA:** open-sourced custom kernels; chunked recurrence unroll for GPU-efficient prefill.
- **Latent expert routing + Quantile Balancing (QB):** MoE load-balancing that solves a constraint-optimization per batch so each expert processes ~q = mk/n tokens.
- **Serving (InferenceX):** benchmarked on real recorded Claude Code traces (median 142k input / 444 output tokens, 65 turns/session). OpenRouter floor $3/M input, $15/M output. Nvidia + AMD both had Day-0 vLLM recipes (DRAM offload, DSpark speculative decode). Model too big for a single B200 node (needs pipeline parallel); fits on one **B300** node (~3.25M-token KV budget before cache thrash).

## Calls
None — architecture deep-dive.
