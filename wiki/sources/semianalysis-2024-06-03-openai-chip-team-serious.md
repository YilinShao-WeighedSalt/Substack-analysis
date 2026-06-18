---
type: source
title: "OpenAI Chip Team Is Now Serious"
tags: []
related: []
created: 2024-06-03
updated: 2024-06-03
authors: [semianalysis]
year: 2024
url: "https://newsletter.semianalysis.com/p/openai-chip-team-is-now-serious"
venue: SemiAnalysis
post_date: 2024-06-03
tickers: [NVDA, AVGO, TSM]
---

[[semianalysis]] argues that OpenAI's in-house chip effort has crossed from rumor into reality: the company went on an aggressive poaching spree, growing its custom silicon team from a handful of engineers to double digits in the months leading up to June 2024. Dylan Patel frames this as a categorical shift — prior actions amounted to talking; now OpenAI is executing.

**Team composition.** OpenAI assembled roughly 20 chip engineers, led by Richard Ho (formerly Google, head of hardware engineering) and Thomas Norrie, both veterans of Google's Tensor Processing Unit (TPU) program. Additional hires were drawn from Apple, Meta, Tesla Autopilot ASIC, and other leading silicon teams, reflecting broad industry poaching rather than a single source.

**Inference focus.** The chip is designed as an inference ASIC — not a training accelerator. This is strategic: as ChatGPT and API products scale, inference compute represents the dominant operational cost. A custom inference chip could cut per-token costs dramatically relative to renting NVIDIA GPUs, and reduce OpenAI's dependence on NVIDIA hardware procurement cycles.

**Partnership structure.** OpenAI is working with Broadcom on ASIC design and targeting TSMC as the manufacturing partner. This mirrors the playbook used by Google (TPU via Broadcom/TSMC) and Amazon (Trainium/Inferentia). Rather than pursuing a full foundry buildout — an idea that circulated in earlier rumors — OpenAI is concentrating on design IP and outsourcing fabrication to TSMC.

**Strategic motivation.** OpenAI's GPU spend ran into billions of dollars annually, with NVIDIA as the near-sole supplier. Custom silicon offers leverage: lower inference cost, better memory bandwidth utilization for transformer workloads, and architectural control over features like in-memory KV-cache management. The inference ASIC would initially serve a portion (~10%) of OpenAI's inference compute; NVIDIA GPUs would remain for training and overflow capacity.

**Competitive context.** Google, Amazon, and Microsoft all run custom silicon programs of several years' maturity. OpenAI's June 2024 hiring surge signals it is finally closing the gap, with a plausible path to first silicon in 2026.

## Calls

- [[NVDA]] — MENTION — n/a — dominant incumbent whose GPUs OpenAI is partially displacing; custom inference ASIC represents a structural long-term headwind to GPU inference demand from hyperscale AI labs
- [[AVGO]] — MENTION — n/a — ASIC design partner for OpenAI's custom inference chip, continuing its established role as the go-to ASIC collaborator for hyperscaler custom silicon programs
- [[TSM]] — MENTION — n/a — manufacturing partner for OpenAI's custom chip, reinforcing TSMC's position as the sole credible advanced-node foundry for AI silicon
