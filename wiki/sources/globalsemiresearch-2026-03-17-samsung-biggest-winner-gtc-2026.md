---
type: source
title: "Nvidia GTC 2026: Is Samsung the biggest winner?"
tags: []
related: []
created: 2026-03-17
updated: 2026-03-17
authors: [globalsemiresearch]
year: 2026
url: "https://globalsemiresearch.substack.com/p/nvidia-gtc-2026-is-samsung-the-biggest"
venue: Global Semi Research
post_date: 2026-03-17
tickers: [NVDA, 005930.KS, TSM]
---

[[globalsemiresearch]] argues that Samsung Electronics is the single biggest beneficiary of the industry transformation announced at NVIDIA's GTC 2026 conference — an event the author dubs the "Super Bowl of AI."

The central event is Jensen Huang's keynote unveiling the **Vera Rubin architecture**, which marks the AI industry's pivot from generative AI (content creation) to inference AI (reasoning, planning, autonomous execution). Huang cited a 1-million-times increase in global AI compute demand over the past two years as context for why the existing architecture was insufficient. The prior CPX product — which only accelerated the Prefill stage — was quietly discontinued, confirming the shift.

**The Groq partnership** is the linchpin of the thesis. NVIDIA announced a deep collaboration with Groq, a specialist inference chip maker, to co-launch the LPX inference rack. The architecture disaggregates inference into two stages: (1) prefill and attention, handled by NVIDIA's Rubin GPUs; (2) token generation, handled by Groq's LPU (Language Processing Unit), which carries massive on-chip SRAM and extremely low latency. The critical detail: Groq's LP30 chip is **exclusively manufactured by Samsung Electronics**, locking Samsung into direct foundry revenue from the new paradigm.

**Quantitative revenue estimate:** 1 LPX rack = 256 LP30 chips; 1 Vera Rubin NVL72 = 1 LPX rack (72:256 GPU:LPU ratio); 1 NVL576 cluster = 5 LPX racks (576:1,280 ratio). Assuming 100,000 LPX rack deployments globally and a ~$3,000 manufacturing cost per LP30 chip, Samsung could generate ~$10 billion in foundry revenue. The author estimates Samsung's total business value per Rubin system (LP30 OEM + HBM + DRAM) is 3–4x that of TSMC's foundry revenue per Rubin GPU (~$1,000–$2,000).

**Storage demand logic:** Groq's built-in SRAM cache does not cannibalize external memory; rather, the inference paradigm shift boosts demand for HBM, DRAM, and SSD — all areas where Samsung has leading positions, further compounding Samsung's advantage over TSMC.

The post does not give explicit price targets or entry prices for any ticker.

## Calls

- [[005930.KS]] — LONG — n/a — Samsung is the exclusive foundry for Groq's LP30 chip and holds full-stack storage exposure (HBM + DRAM + SSD), making it the biggest beneficiary of NVIDIA's Vera Rubin / disaggregated inference architecture
- [[NVDA]] — MENTION — n/a — Vera Rubin architecture and GTC 2026 announcements are the primary catalyst for the entire thesis; NVIDIA itself is not the focus of the call
- [[TSM]] — MENTION — n/a — Referenced as a comparison point; Samsung's total system value per Rubin deployment is estimated at 3–4x TSMC's foundry revenue, implying TSMC is a relative loser in this configuration
