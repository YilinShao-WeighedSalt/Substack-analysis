---
type: source
title: "The Coding Assistant Breakdown: More Tokens Please"
tags: []
related: []
created: 2026-04-24
updated: 2026-04-24
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/the-coding-assistant-breakdown-more"
venue: SemiAnalysis
post_date: 2026-04-24
tickers: []
---

[[semianalysis]] delivers a detailed benchmark and economics breakdown of the coding assistant landscape in April 2026, arguing that cost-per-task — not cost-per-token — is the correct framework for evaluating AI model procurement, and that published benchmarks are structurally unreliable.

**GPT-5.5 marks a frontier shift — at a price.** OpenAI's GPT-5.5 is assessed as "materially better at some tasks than all other models," ending months of Anthropic Opus dominance. However, pricing jumped to $5 input / $30 output per million tokens — 2× its predecessor — and a priority-tier multiplier of 2.5× over standard rates is becoming an important revenue lever for both OpenAI and Anthropic.

**Cost-per-task is the true north star.** The central thesis reframes how enterprise buyers should evaluate models. An expensive model that completes a task in fewer tokens can deliver better economics than a cheaper model requiring more. SemiAnalysis measured input/output token ratios for coding workloads: Codex runs at ~80:1 and Claude Code at ~100:1. This asymmetry means output token pricing dominates real-world costs and makes headline per-million rates misleading.

**Opus 4.7 — incremental, not transformative.** Anthropic's Opus 4.7 update added high-resolution image support, reasoning controls, and task budgets, but did not deliver a capability step-change. More significantly, a new tokenizer increased token consumption by up to 35%, effectively raising prices. SemiAnalysis disclosed a postmortem in which three bugs affected Claude Code users for weeks (March–April), highlighting how product harness issues can be misattributed to model quality.

**DeepSeek V4 is a strong open-source challenger.** DeepSeek V4-Pro (1.6T total / 49B active parameters) and V4-Flash (284B / 13B) expand context from 128k to 1M tokens and achieve ~90% KV cache reduction versus V3 via Compressed Sparse Attention. Throughput on H200 at FP8 reaches ~150 tokens/sec. V4-Pro fits within 8× H20 HGX memory at FP4, keeping inference accessible outside NVIDIA's highest-tier hardware.

**Benchmark contamination is systemic.** The analysis documents multiple reliability failures: MMLU saturation (GPT-4 reached 86.4% in March 2023), HLE chemistry/biology conflicts with peer-reviewed literature (~30% of answers), and SWE-bench's reduction from 2,294 to 500 verified problems. Expert-SWE results: Opus 4.7 scored 71.8%, Mythos 77.8%; GPT-5.5 results were withheld by OpenAI because Opus 4.7 outperformed it — exactly the selective reporting dynamic the piece criticizes. Labs optimizing against contaminated benchmarks during training creates a self-defeating cycle that clouds true capability assessment.

**Market consolidation fears may be overblown.** DeepSeek's open-source release has not commoditized frontier closed-source models; capability gaps persist and justify premium pricing. The emergence of priority-tier API tiers signals that frontier labs are gaining pricing power in high-value enterprise coding workflows.

## Calls

