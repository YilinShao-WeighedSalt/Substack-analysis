---
type: source
title: "DeepSeek Debrief: >128 Days Later"
tags: []
related: []
created: 2025-07-03
updated: 2025-07-03
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/deepseek-debrief-128-days-later"
venue: SemiAnalysis
post_date: 2025-07-03
tickers: [NVDA, AMD, AMZN, GOOGL, BIDU, BABA]
---

[[semianalysis]] revisits DeepSeek R1 roughly 150 days after its January 2025 launch, assessing whether the initial market shock translated into durable disruption.

**Consumer traction faded; API adoption surged.** DeepSeek's own consumer app traffic peaked and then declined in both relative and absolute terms, while ChatGPT, Claude, and Gemini grew strongly over the same period. Paradoxically, R1/V3 usage on third-party hosting platforms grew ~20x since release — DeepSeek's influence is felt through the open-source ecosystem, not through its own product.

**Tokenomics framework.** The post introduces three KPIs — latency/time-to-first-token, interactivity (tokens/sec), and context window — arguing that $/million-tokens is merely a dependent variable shaped by these levers. DeepSeek deliberately maximizes batch sizes, reducing per-token cost at the expense of multi-second first-token latency and a 64K context ceiling (among the smallest of major providers). This reflects a strategic choice: DeepSeek's priority is internal AGI R&D, not monetizing end-user traffic. Open-sourcing preserves internal compute while building global mindshare.

**Anthropic's compute pressure.** Claude 4 Sonnet throughput dropped ~40% since launch to ~45 tokens/sec, caused by heavy batching as Claude Code usage exploded. The article notes Anthropic compensates through superior token efficiency — Claude produces 3x fewer output tokens than Gemini 2.5 Pro, Grok 3, or DeepSeek R1-0528 for equivalent tasks, optimizing for intelligence-per-token rather than raw speed. Infrastructure deals in progress: Amazon committed 500K+ Trainium chips (though Claude 4 was trained on GPUs/TPUs, not Trainium), and Google Cloud provides TPU rental capacity.

**Google Cloud expansion.** Google struck a GPU rental deal with OpenAI and is expanding its AI cloud offerings. Gemini CLI now offers free, generous request limits to compete directly with Claude Code.

**Chinese model ecosystem.** Despite export controls constraining inference capacity, Chinese training pipelines remain competitive. Tencent (Hunyuan-A13B), Alibaba (Qwen3), Baidu (ERNIE 4.5), and Rednote all released notable models in the period, demonstrating that export controls have not materially slowed frontier training progress in China.

**Emerging token-as-a-service economy.** Specialized AI coding tools — Cursor, Windsurf, Replit, Perplexity — are monetizing through token consumption rather than flat subscriptions, mirroring Anthropic's API-first strategy versus OpenAI's bundled ChatGPT Plus model.

## Calls

- [[NVDA]] — MENTION — px@call n/a — cited in AMD/NVIDIA benchmarking of DeepSeek hardware batching strategy; no explicit directional view
- [[AMD]] — MENTION — px@call n/a — cited alongside NVDA in inference benchmarking; no explicit directional view
- [[AMZN]] — MENTION — px@call n/a — 500K+ Trainium chip commitment to Anthropic signals AWS inference ambitions, though chips are work-in-progress
- [[GOOGL]] — MENTION — px@call n/a — provides TPU rental to Anthropic and struck GPU deal with OpenAI; expanding cloud AI offerings and competing on Gemini CLI
- [[BIDU]] — MENTION — px@call n/a — ERNIE 4.5 release cited as evidence Chinese frontier model development continues despite export controls
- [[BABA]] — MENTION — px@call n/a — Qwen3 release cited alongside other Chinese model launches
