---
type: source
title: "Anthropic Subscriptions Offer 5x+ More Value Than OpenAI"
tags: []
related: ["[[semianalysis]]", "[[ai-software-models]]"]
created: 2026-10-08
updated: 2026-10-08
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/anthropic-subscriptions-offer-5x"
venue: SemiAnalysis
post_date: 2026-10-05
tickers: []
---
Paywalled post, full body served. An economics deep-dive on consumer/SMB AI **subscription limits** and what they imply for lab financials — **no priced ticker call** (Anthropic, OpenAI, and the Chinese labs are private). Ingested for domain knowledge (→ [[ai-software-models]]).

Core argument: subscription plans are heavily subsidized but matter disproportionately — for Anthropic, subscriptions are **~10% of revenue yet >40% of inference compute**, lowering blended **revenue per MW by ~$36M**. To model lab financials you must understand limits, which work as "credits" where each (model, token-type) combo burns a different amount, so a plan's worth is only meaningful as a **(plan, model, workload) tuple**. SemiAnalysis launched a **Subscriptions Dashboard** (Tokenomics Model subscribers) that re-measures every (plan, model, token-type) daily across OpenAI, Anthropic, Meta, SpaceXAI, Cursor, Cognition, Z.ai, MiniMax, Moonshot.

Methodology: token types = input / cache-write / cache-read / output (plus expensive long-context tiers); they reverse-engineer each plan's 0–100% meter by isolating one token type at a time (War-and-Peace prompts for input, a technical essay for output) and watching meter steps, tracking a ±5% range. They caught a provider running an **"extremely tiny" A/B test** on limits — proving providers can silently change limits, and that the method is sensitive enough to detect it.

Headline results:
- **Anthropic ~5× the API-equivalent value of OpenAI** at the mid-tier daily-driver models (Opus 5.5 vs GPT-6.1 Sol); Fable 5.1 can only use 50% of the limit but the gap persists even on raw tokens. "Opus 5.5 on any Claude subscription offers far better value than anything from OpenAI."
- **OpenAI just halved the $200 plan's API-equivalent value** and added a **$500 tier** (300 TPS Ultrafast the headline). Existing $200 plans keep old limits until Oct-29; new ones start lower. The new $500 plan only offers ~21% more Astra than the old $200.
- Two margin strategies: **Anthropic** quietly cuts API-equivalent value on more-premium models (Opus 5.5 at 100% util ≈ -369% GM vs Fable 5.1 ≈ 1%; at 20% util, 6% vs 80%) — "software-like margins if everyone used Fable." **OpenAI** took the "nuclear option," cutting to Fable-level limits across the board but avoided public backlash.
- **Chinese subscription plans** are still a good deal and, unusually, value-per-dollar *rises* with higher tiers (but overall less than the ~12x OpenAI). First-party plans beat third-party wrappers (Cursor/Devin).

Concept color for the decoder: **API-equivalent value**, **revenue per MW**, subscription credits, cache-read/write token pricing.

## Calls
- None (private companies; economics/methodology deep-dive). Read-through: Anthropic's subscription value-leadership and OpenAI's limit cuts are inputs to lab tokenomics; no tradeable ticker.
