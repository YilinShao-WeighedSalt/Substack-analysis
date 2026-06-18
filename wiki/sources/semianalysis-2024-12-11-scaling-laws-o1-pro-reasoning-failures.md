---
type: source
title: "Scaling Laws - O1 Pro Architecture, Reasoning Training Infrastructure, Orion and Claude 3.5 Opus Failures"
tags: []
related: []
created: 2024-12-11
updated: 2024-12-11
authors: [semianalysis]
year: 2024
url: "https://newsletter.semianalysis.com/p/scaling-laws-o1-pro-architecture-reasoning-training-infrastructure-orion-and-claude-3-5-opus-failures"
venue: SemiAnalysis
post_date: 2024-12-11
tickers: [NVDA, GOOGL, META, AMZN]
---
[[semianalysis]] argues that scaling laws are far from dead — they are evolving across multiple new dimensions beyond pre-training, including post-training optimization, synthetic data generation, reinforcement learning, and inference-time compute scaling. The widespread "end of scaling" narrative is compared to the circa-2008 discourse about CPU clock speed limits: when one scaling vector saturates, the industry pivots to new ones rather than stalling.

**Pre-training challenges and responses.** Public internet text has effectively been exhausted as a training source, and saturated benchmarks (e.g., MMLU) no longer discriminate frontier model capability. The response has been harder evals (GPQA Diamond, FrontierMath, SWE-Bench Verified) and new data sources. Meta holds an estimated 100x more proprietary data than the public internet. YouTube's 720,000 hours of daily video uploads represent a largely untapped resource. Synthetic data generation is scaling to billions of tokens and increasingly fills the gap.

**Post-training as a new scaling frontier.** The article details how supervised fine-tuning (SFT), RLHF/RLAIF, PPO, DPO, and Constitutional AI each unlock additional capability gains independent of pre-training compute. Meta reportedly spent $10–20 million on preference data for Llama 2 alone. Process Reward Models (PRM) versus Outcome Reward Models (ORM) are explored as mechanisms for guiding reasoning chains at training time.

**Inference-time scaling and o1.** OpenAI's o1 and o1 Pro are cited as proof-of-concept that compute spent at inference — through chain-of-thought reasoning, Best-of-N sampling, self-consistency, and Monte Carlo tree search rollouts — produces meaningful capability jumps. On GPQA Diamond, o1 scored 78% versus ~70% for PhD-level humans, compared to 39% for GPT-4 with search. On FrontierMath, best models sit at ~2% today; Anthropic projects 80% capability achievable medium-term. Nvidia's GB200 NVL72 rack architecture is highlighted as the hardware platform enabling economical inference-time scaling.

**The "failures" narrative corrected.** Claude 3.5 Opus was not a scaling failure — it scaled as expected but was repurposed internally for synthetic data generation and reward modeling rather than released publicly, because inference economics made broad deployment unviable at that capability tier. Similarly, concerns about OpenAI's Orion project were characterized as misrepresented in press coverage.

**Capex as revealed preference.** Amazon's Project Rainier (400,000 Trainium2 chips, ~$6.5B estimated investment for Anthropic), Meta's 2 GW datacenter plans for Louisiana by 2026, and Google's and Microsoft's multi-datacenter training buildouts are treated as the strongest evidence that hyperscalers remain convinced scaling returns are positive.

## Calls

- [[NVDA]] — LONG — n/a — GB200 NVL72 is the primary hardware platform for inference-time scaling, which the post identifies as the next major compute scaling vector
- [[AMZN]] — MENTION — n/a — investing ~$6.5B in 400k Trainium2 chips for Anthropic (Project Rainier), demonstrating conviction in continued scaling
- [[META]] — MENTION — n/a — 2 GW datacenter buildout planned for Louisiana by 2026; holds ~100x public internet data volume as a training moat
- [[GOOGL]] — MENTION — n/a — aggressive multi-datacenter training infrastructure investment; DeepMind benchmarks (GPQA Diamond) cited as capability milestones
