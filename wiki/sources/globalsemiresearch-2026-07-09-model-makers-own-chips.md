---
type: source
title: "Why the Model Makers Are Coming for Their Own Chips"
tags: [custom-silicon-asic, ai-software-models, inference, nvidia-gpu-platform]
related: ["[[globalsemiresearch]]", "[[custom-silicon-asic]]", "[[ai-software-models]]", "[[nvidia-gpu-platform]]", "[[NVDA]]", "[[AVGO]]"]
created: 2026-07-10
updated: 2026-07-10
authors: [globalsemiresearch]
year: 2026
url: "https://globalsemiresearch.substack.com/p/why-the-model-makers-are-coming-for"
venue: Global Semi Research
post_date: 2026-07-09
tickers: [NVDA, AVGO]
---

# Why the Model Makers Are Coming for Their Own Chips

Deep dive (partly paywalled) arguing that DeepSeek, OpenAI, and Anthropic all edging into custom silicon is **not** a "short Nvidia" trade — it's a signal that AI's cost structure has flipped from training to **inference**.

Key framing: **"Training is a capex event. Inference is the electricity bill."** Training is a bounded one-time investment; inference is a perpetual operating cost that scales with revenue. Every chat/completion/agent step re-reads context (the **KV cache**) and generates tokens, consuming compute, HBM, interconnect, power. Success makes it worse — more capable models get trusted with longer contexts → each request costs more to serve. For the labs, the chip bill now sits directly under gross margin, latency, and pricing power.

Three signals in months: (1) **OpenAI + Broadcom "Jalapeno"** (first "Intelligence Processor," LLM inference, deploy late 2026, unveiled Jun 24); (2) **Anthropic** exploring own chip designs (Reuters, April; no committed team disclosed); (3) **DeepSeek** developing own inference chip (Reuters, Jul 7) to cut reliance on Nvidia AND Huawei.

Technical "why now": DeepSeek V3 (Dec 2024) trained on 2,048 Nvidia H800; V4 (Apr 2026) adapted to Huawei Ascend 950. V4-Pro = 1.6T params / 49B active; V4-Flash = 284B / 13B active; both 1M-token context. At 1M tokens the bottleneck is memory capacity/bandwidth/data-movement, not FLOPs. V4-Pro claims ~27% of the per-token inference compute and ~10% of the KV cache of V3.2 — evidence the architecture is already contorted to minimize data movement, so a general-purpose GPU becomes "flexibility you no longer need." Same logic for Jalapeno (emphasizes memory movement, networking, serving patterns over headline compute).

Strategic inversion: for a decade model builders adapted software to the GPU; now the frontier labs define what the chip should optimize. Workload knowledge is proprietary data finally being spent. Piece paywalls before its "three companies, three levels of commitment" ranking.

## Calls
- [[NVDA]] — **NEUTRAL (defended vs. short)** @ ~$195.84 (mark 07-06; live egress-blocked) — custom inference chips attack the stable/high-volume slice, not the volatile frontier where GPUs win; "short Nvidia" read is wrong/premature.
- [[AVGO]] — **LONG (implied beneficiary)** @ ~$369.34 (mark 07-02) — enabler of the wave (built Jalapeno; reported Anthropic partner); more model-maker silicon = more Broadcom design work.
- Read-through: bearish **Huawei** (DeepSeek domestic chip displaces Ascend, not Nvidia, in China).
