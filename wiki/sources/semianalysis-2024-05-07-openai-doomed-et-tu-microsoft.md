---
type: source
title: "OpenAI Is Doomed? - Et tu, Microsoft?"
tags: []
related: []
created: 2024-05-07
updated: 2024-05-07
authors: [semianalysis]
year: 2024
url: "https://newsletter.semianalysis.com/p/openai-is-doomed-et-tu-microsoft"
venue: SemiAnalysis
post_date: 2024-05-07
tickers: [MSFT, META, GOOGL, NVDA]
---

[[semianalysis]] (Dylan Patel and Daniel Nishball) argues that OpenAI faces existential competitive pressure from multiple directions simultaneously — and that its most dangerous threat is not a rival AI lab but its own primary backer, Microsoft.

**Model commoditization is accelerating.** As of May 2024, multiple firms — Google (Gemini 1.5 Ultra), Meta (Llama 3 405B), and China's DeepSeek V2 — are within striking distance of GPT-4 on Chatbot ELO. DeepSeek V2, an open-source MoE model (236B total / 21B active parameters, trained on 8.1T tokens), achieves GPT-4-class performance at 1/20th the training FLOPs of GPT-4. Its inference economics are particularly disruptive: at ~$15/hour for an 8xH800 node and peak throughput of 50,000 decode tokens/second, DeepSeek can earn 70%+ gross margins at API pricing that undercuts every Western provider including GPT-3.5 Turbo.

**Microsoft is quietly building an exit ramp.** Microsoft is committing >$50B annually to AI datacenter capex, but the majority is being directed to internal workloads — not OpenAI. The structural reason: OpenAI's nonprofit board can unilaterally declare AGI has been achieved, instantly voiding all commercial and IP licensing agreements with Microsoft. With zero board voting rights, Microsoft has no recourse. In response, Microsoft is: (1) acquiring the Inflection AI pretraining team and dataset to bootstrap MAI-1, a ~500B parameter MoE targeting GPT-4 class by end of May 2024; (2) deploying Phi-3 (small models via synthetic data) and WizardLM's Evol-Instruct for instruction tuning; and (3) planning a 100K GPU cluster (5x the GPT-4 training cluster) for internal research. More than 65% of Fortune 500 already uses Azure OpenAI — Microsoft can redirect these workloads to its own models without OpenAI gaining.

**Distribution vs. compute as the strategic moat.** Meta's open-source strategy (Llama 3) is already deployed across Facebook, Instagram, and WhatsApp in 14 countries reaching 1.1B people, with a 3.24B DAU base as the eventual target. Google holds a potential trump card via an Apple deal to deploy Gemini natively on iPhone — replicating its search dominance playbook. Google also leads on custom silicon (TPU buildout pace) and has unified training under Google DeepMind. NVIDIA H100 rental pricing is falling monthly as medium-sized cluster availability grows, compressing OpenAI's inference cost advantage.

**Authors' bottom line:** Despite the bearish framing, the authors state they do not believe OpenAI is doomed — the piece is a structured bear case ahead of next-generation model announcements. The real risk is if capital and compute scale are all that matter, in which case Google leads; if distribution is king, Meta and Google both dominate; if neither, OpenAI's IP-carveout structure with Microsoft becomes its Achilles heel.

## Calls

- [[MSFT]] — NEUTRAL — n/a — Strategically hedging OpenAI dependence by building MAI-1 and redirecting capex to internal models; governance risk from OpenAI's AGI carve-out clause forces contingency planning
- [[META]] — MENTION — n/a — Open-source Llama 3 strategy and Meta AI rollout to 3B+ users positions Meta as a distribution-dominant AI player that threatens OpenAI's consumer mindshare
- [[GOOGL]] — MENTION — n/a — TPU buildout pace, unified DeepMind team, and potential Apple Gemini deal make Google the capital/compute/distribution leader among OpenAI challengers
- [[NVDA]] — MENTION — n/a — H100/H800 rental pricing falling monthly as cluster availability grows; DeepSeek's H800-based inference economics highlight the commoditization pressure on GPU-dependent inference businesses
