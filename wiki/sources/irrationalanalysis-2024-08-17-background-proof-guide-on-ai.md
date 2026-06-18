---
type: source
title: "A Background-Proof Guide on AI"
tags: []
related: []
created: 2024-08-17
updated: 2024-08-17
authors: [irrationalanalysis]
year: 2024
url: "https://irrationalanalysis.substack.com/p/a-background-proof-guide-on-ai"
venue: Irrational Analysis
post_date: 2024-08-17
tickers: [NVDA, AVGO, QCOM, MU, MRVL, TSLA]
---

[[irrationalanalysis]] delivers a DSP-engineer's intuition-driven primer on ML/AI fundamentals, tracing the field from the 1943 Perceptron through the 2012 AlexNet revolution and the 2017 transformer era. The author frames AI as linear-algebra spam at its core — matrix multiplications, sparse activation functions (ReLU), gradient descent in trillion-dimensional space — and draws an illuminating analogy to JPEG compression: both use linear algebra to perform lossy compression, trading information loss for size. Training differs from inference primarily in memory footprint (storing intermediate activations for backpropagation) and the need for automatic differentiation (chain-rule spam), not just matmuls.

Key first-principles observations on AI systems: (1) Complexity is always conserved — "simple" hardware shifts complexity to the compiler (Groq, Cerebras). (2) Open standards are not inherently superior; Nvidia's proprietary 224G NVLink beat every competitor to market by a year by ignoring irrelevant telco temperature specs. (3) Scaling is primarily limited by memory and interconnect bandwidth, not raw compute. (4) "Scaling laws" are empirical extrapolations, not mathematical proofs like the Cramer-Rao bound or Shannon-Hartley theorem. (5) AI ASICs for general sale have an almost zero historical success rate; hyperscaler semi-custom chips (TPU, MTIA) are not real ASICs because they are not sold horizontally. Startups like Etched and Taalas face a timing trap: 12–18 month chip development cycles in a field where model architectures shift weekly.

On the investment side as of August 2024, the author's highest-conviction longs are NVDA (~40% of portfolio) and AVGO (~20%), with AVGO defended on its irreplaceable custom-silicon moat and 224G SerDes leadership — the author dismisses rumors of MediaTek winning Google's next TPU SerDes as fantasy given MTK's signal-integrity limitations. QCOM is actively shorted to lever up the AVGO position. MU and MRVL 2025 OTM calls are small speculative positions: the MU thesis rests on an impending DDR5 demand surge from CPU socket consolidation driving power savings in hyperscaler campuses, plus a possible AI-induced NAND crunch; MRVL catalysts include a large Amazon Trainium/Inferentia ramp, optical DSP growth, and potentially sandbagged guidance. TSLA is mentioned critically in the context of Elon Musk using Tesla equity to fund xAI's duplicative GPU spend.

The author closes with a broader macro warning: the AI infrastructure wave is a DotCom 2.0 bubble, fueled not by debt-laden startups (as in 2000) but by cash-rich hyperscalers alongside a frothy layer of neo-clouds (Coreweave), zombie AI hardware companies (Graphcore), and dozens of duplicative LLM labs — and the bubble will get significantly larger before it collapses.

## Calls

- [[NVDA]] — LONG — px@n/a — Highest-conviction position (~40% of portfolio); GPU dominance in AI training driven by AlexNet legacy and proprietary CUDA/NVLink ecosystem
- [[AVGO]] — LONG — px@n/a — Second-highest conviction (~20% of portfolio); unrivaled custom-silicon moat, 224G SerDes leadership secures Google TPU relationship through at least 2028
- [[QCOM]] — SHORT — px@n/a — Shorted to lever up AVGO exposure; no specific bear thesis elaborated beyond capital allocation
- [[MU]] — LONG — px@n/a — Small speculative call option; DDR5 demand surge from CPU socket consolidation and potential AI-driven NAND crunch
- [[MRVL]] — LONG — px@n/a — Small speculative call option; Amazon Trainium/Inferentia ramp, optical DSP buildout, possible guidance sandbagging
- [[TSLA]] — MENTION — px@n/a — Cited critically as vehicle Musk may use to fund xAI's uneconomic duplicative GPU CapEx
