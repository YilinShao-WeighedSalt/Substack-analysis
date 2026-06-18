---
type: source
title: "DeepSeek Debates: Chinese Leadership On Cost, True Training Cost, Closed Model Margin Impacts"
tags: []
related: []
created: 2025-01-31
updated: 2025-01-31
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/deepseek-debates"
venue: SemiAnalysis
post_date: 2025-01-31
tickers: [NVDA, GOOGL, META]
---

[[semianalysis]] pushes back on the dominant DeepSeek narrative that swept global markets in late January 2025. The post argues that the widely cited "$6M training cost" for DeepSeek V3 is a severe misrepresentation — that figure covers only the final pre-training GPU compute run, excluding R&D, architecture ablations, synthetic data generation for post-training, and hardware TCO. The authors estimate DeepSeek's total hardware spend exceeds $500M, with ~$1.6B in total server CapEx across High-Flyer and DeepSeek combined. They believe the lab controls roughly 50,000 Hopper-class GPUs (a mix of H100, H800, and H20), not a lean operation enabled purely by algorithmic efficiency.

On model performance, the post contextualizes DeepSeek V3 against GPT-4o (released May 2024) rather than frontier models — noting that cost and capability improvements of this magnitude are expected over an eight-month window given ~4x annual algorithmic progress. R1's match with o1 is more impressive given the shorter gap, but the authors attribute this to reasoning being a new paradigm with lower-hanging fruit via RL and synthetic data post-training. They note R1's paper omits compute figures deliberately, as RL at scale required far more GPU hours than the narrative suggests.

Key technical innovations highlighted: Multi-Head Latent Attention (MLA), which reduces KV Cache by 93.3% versus standard attention and is the primary driver of DeepSeek's low inference cost; Mixture-of-Experts with efficient token routing; Multi-Token Prediction in pre-training; and FP8 training (already in use at leading US labs). The authors expect MLA to be rapidly copied by Western labs.

On market implications, the post notes that H100/H200 pricing has actually risen due to induced demand from cheaper inference — early evidence of Jevons paradox. DeepSeek is assessed to be subsidizing inference pricing to gain market share and not yet profitable on inference. Google's Gemini Flash 2.0 Thinking is flagged as cheaper than R1 and competitive on benchmarks, receiving none of the hype due to poor go-to-market execution. Export controls are identified as a structural constraint for future Chinese GPU acquisition, with the H20 now the only China-available Nvidia chip.

## Calls

- [[NVDA]] — LONG — n/a — H100/H200 pricing rising on induced inference demand; Jevons paradox supports continued GPU capex despite efficiency gains
- [[GOOGL]] — MENTION — n/a — Gemini Flash 2.0 Thinking is cheaper and competitive with R1 but receives no hype due to poor go-to-market
- [[META]] — MENTION — n/a — Cited as losing to DeepSeek on open reasoning model release despite larger resources
