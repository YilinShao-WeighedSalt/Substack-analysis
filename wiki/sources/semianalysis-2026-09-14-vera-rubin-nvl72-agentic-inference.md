---
type: source
title: "Vera Rubin NVL72 Agentic Inference: 67x better Performance per Dollar"
tags: [nvidia, vera-rubin, inference, agentx, tco, perf-per-watt, amd]
related: ["[[semianalysis]]", "[[NVDA]]", "[[AMD]]", "[[nvidia-gpu-platform]]", "[[ai-accelerator-competition]]", "[[hbm-memory]]"]
created: 2026-09-17
updated: 2026-09-17
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/vera-rubin-nvl72-agentic-inference"
venue: SemiAnalysis
post_date: 2026-09-14
tickers: [NVDA, AMD]
---

First verified third-party Rubin results on SemiAnalysis's AgentX agentic-inference benchmark, on early pre-release TRTLLM software.

**Headline.** Vera Rubin NVL72 delivers **~67x total tokens per $ TCO vs GB300 Dynamo TRTLLM** at 170 TPS (owning-cost basis), and **1.4-3x** across the realistic 60-100 TPS serving band. On perf/MW: **up to 7x** token throughput/MW vs Blackwell (Jensen claimed only 3x at GTC 2026 — "sandbagging" as he did in 2024 when GB200's claimed 30x vs Hopper tested at 98x). ~61% higher max P90 interactivity than GB300 (276 vs 172 TPS). Against B300/H200 the gap widens further (10x tokens/$ vs B300 at 80 TPS; 18-39x vs H200). Production SKU: 2300W TDP, 1.5TB LPDDR5X/tray (Nvidia halved Vera memory).

**Economics.** At 75 TPS, 60% util, no license fee (DeepSeek V4 Pro 1.6T MIT proxy): **$159.5B revenue / $149.9B modeled profit per all-in GW** vs GB300 Dynamo SGLang $114.9B/$105.3B → **+39% revenue / +42% profit per GW** (~$446M more profit/GW at 10MW). Alternatively ~28% pricing headroom. New **DSX MaxLPS** dynamic power-shifting lets operators fit more GPUs per datacenter power footprint. Verdict: "if you have the money to buy or rent a VR NVL72, you should."

**Nuance.** AMD's MI455X UALoE72 has committed to collaborating on AgentX; benchmark is corroborated by Google Cloud, Azure, Oracle, Meta, OpenAI, and the ML community (vLLM/SGLang/PyTorch/HF). Falsifier: this is pre-release software; the gap could compress rather than widen as competing stacks mature.

## Calls
- **[[NVDA]] LONG $213.90** — Rubin's perf/TCO and perf/MW lead is decisive; buy/rent it.
- **[[AMD]] NEUTRAL $512.50** — MI455X in the benchmark, but Rubin owns the frontier.
