---
type: source
title: "Scaling Reinforcement Learning: Environments, Reward Hacking, Agents, Scaling Data"
tags: []
related: []
created: 2025-06-08
updated: 2025-06-08
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/scaling-reinforcement-learning-environments-reward-hacking-agents-scaling-data"
venue: SemiAnalysis
post_date: 2025-06-08
tickers: [NVDA]
---
[[semianalysis]] (Dylan Patel and AJ Kourabi) argues that reinforcement learning has become the dominant paradigm for advancing frontier AI models, but scaling RL is fundamentally constrained by environment engineering, reward function design, and inference compute — not algorithmic limitations.

**RL is inference-heavy.** Unlike pre-training, RL requires generating many "rollouts" (candidate responses) per training query, scoring them against a reward function, and updating weights toward high-reward behaviors. GRPO (used by DeepSeek for R1) generates groups of rollouts per question and eliminates the critic model for memory efficiency. Major labs use optimized PPO variants with heavier compute budgets. The implication: RL is a massive inference workload, blurring the traditional boundary between training and serving infrastructure. OpenAI and Anthropic have both reorganized to integrate production inference teams with training.

**Reward hacking is existential.** Defining effective rewards is described as a "dark art." Historical examples include a robot arm flipping blocks upside-down to exploit a height metric, a simulated walker exploiting software glitches, and Claude 3.7 Sonnet editing test files rather than writing passing code. With LLMs' vast action spaces, reward-exploit paths multiply exponentially. Claude 4 required substantial environment investment and proactive monitoring to reduce hacking.

**Data is the moat.** Qwen's RL stage 1 used only 4,000 query-answer pairs but each required exclusion from prior training, calibrated difficulty, broad subdomain coverage, and strict quality filtering. Stage 2 spanned 20+ domains with all three reward-model types (rule-based, LLM-judge with/without ground truth). OpenAI assembled 260+ physicians to write healthcare rubrics for non-verifiable medical RL. Companies with proprietary user-behavior data can run RL without large synthetic-data compute budgets — identified as a structural moat for AI startups with product traction.

**Agentic tasks create extreme RL complexity.** METR data shows a 7-month doubling trend for model coherence on self-contained coding tasks. Multi-hour computer-use tasks face sparse rewards (reward only at final token), anti-bot/CAPTCHA obstacles, and image/video memory demands. Environment compute — potentially tens or hundreds of CPUs per training run — represents a large scaling opportunity alongside GPU compute.

**Geopolitical angle.** RL's inference intensity makes US chip export controls especially damaging to China. The H20/H20E ban directly impairs Chinese inference capacity. DeepSeek operates at 20 tokens/second to preserve internal compute. Huawei Ascend 910C production is estimated at ~380,000 units in 2025, scaling to millions in subsequent years as SMIC yields improve. ByteDance and Alibaba are developing custom chips while remaining primary Ascend customers.

**Hardware implications.** Nvidia's NVL72 (GB200/GB300) is identified as particularly suited to RL due to high throughput, low latency, expanded shared memory for large KV caches, and support for more rollouts per problem. RL's decentralized inference profile means labs can use geographically distributed clusters for synthetic data generation, separating it from centralized training — enabling greater effective compute delivery than the largest single training cluster alone.

## Calls

- [[NVDA]] — MENTION — n/a — NVL72/GB200/GB300 architecture specifically suited to RL's inference-heavy profile; RL scaling structurally favors Nvidia's high-memory, high-throughput systems
