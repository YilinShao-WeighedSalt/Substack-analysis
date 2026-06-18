---
type: source
title: "RL Environments and RL for Science: Data Foundries and Multi-Agent Architectures"
tags: []
related: []
created: 2026-01-06
updated: 2026-01-06
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/rl-environments-and-rl-for-science"
venue: SemiAnalysis
post_date: 2026-01-06
tickers: []
---
[[semianalysis]] argues that post-training reinforcement learning (RL) compute — not pre-training scale — has driven the most significant AI capability gains over the past 18 months. OpenAI's use of the same GPT-4o base model across o1, o3, and the GPT-5 series is the central evidence: all performance improvements during that window stemmed from scaling RL compute in post-training, not from larger foundation models.

**RL data construction as a new industry.** Unlike pre-training, which ingested the open internet, RL training requires purpose-built task environments constructed from scratch. This bottleneck has spawned a fragmented ecosystem of over 35 environment vendors across domains: UI gyms (priced at roughly $20,000 per website replica), platform environments (Slack, Salesforce, AWS, Gmail, Discord), and coding environments (highest demand). Notable vendors include Habitat, DeepTune, Fleet, Vmax, Turing, Mechanize, and HUD.

**Data foundries as the talent intermediary.** Contractor platforms — Mercor, Handshake, Surge (estimated ~$1B ARR), and Aboda.ai — have repositioned from job-matching to servicing the lab-to-domain-expert pipeline. Scale AI's historic role (>$1.4B 2024 revenue) has been disrupted: Meta absorbed much of its capacity, causing competing labs to reduce contracting to avoid sharing priority data pipelines with Meta.

**Lab procurement postures diverge.** Anthropic is the most aggressive buyer, working with 12+ environment vendors, actively building an open vendor ecosystem to commoditize costs, and expanding into biology and computer-use alongside coding. OpenAI uses a narrower vendor pool with higher per-vendor spend, is internalizing human data teams, and deploys spending across UI gyms, reasoning, and consumer behavioral training. Google DeepMind procures decentrally by research team, had under 5% post-training compute at Gemini 2.5 Pro launch, and benefits from owning the underlying platforms (Sheets, Slides, Docs) natively.

**RL for science.** OpenAI targets early-stage biology discovery via autonomous closed-loop systems where models propose protocols, receive experimental results, and iterate without human intervention. Anthropic is building Claude for Life Sciences, an enterprise platform with connectors to Benchling, 10x Genomics, and PubMed. Key infrastructure enablers: Periodic Labs (closed-loop RL grounded in physical experiments) and Medra (robotically automated lab generating validated biological data). DeepMind is establishing an automated materials science research lab in 2026. Sparse-reward problems from long experimental timelines (days) are addressed via rubric-based intermediate step rewards; in-flight weight updates can double RL iteration speed.

**RL-as-a-service and platform dynamics.** Startups (RunRL, Osmosis, Applied Compute, Adaptive ML) offer custom post-training to enterprises, undercutting OpenAI's RFT service by ~5x, often using Qwen base models. OpenAI's "Instant Checkout" (Shopify/Etsy integration) previews agent-commerce monetization. Amazon blocked ChatGPT Agent access to its shopping platform; OpenAI negotiates platform access via cloud and chip partnership deals.

**China context.** Chinese labs (Qwen at ~5% post-training compute) are under-scaled on RL relative to Western peers. VC-backed domestic data foundries aim to serve local labs at lower cost than Western providers; Surge is reportedly active with Moonshot and Z.ai, and environment access contributed to capability gains in Kimi K2 and GLM-4.6.

## Calls

_No exchange-listed tickers receive an explicit investment stance in this post. All named companies (Scale AI, Mercor, Surge, Mechanize, Periodic Labs, Medra, RunRL, etc.) are private._
