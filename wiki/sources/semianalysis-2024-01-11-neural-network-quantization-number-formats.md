---
type: source
title: "Neural Network Quantization & Number Formats From First Principles"
tags: []
related: []
created: 2024-01-11
updated: 2024-01-11
authors: [semianalysis]
year: 2024
url: "https://newsletter.semianalysis.com/p/neural-network-quantization-and-number"
venue: SemiAnalysis
post_date: 2024-01-11
tickers: []
---

[[semianalysis]] makes the case that quantization — reducing the bit-precision of neural network weights and activations — has become one of the most commercially significant forces in AI hardware. Nvidia estimates quantization has contributed 16x of a total 1000x improvement in single-chip compute over the past decade, dwarfing the 2.5x gained by shrinking process nodes from 28nm to 5nm. The Google BF16 litigation (estimated $1.6–5.2B) underscores how high the stakes around number formats have become.

The piece builds from first principles. It covers unsigned/signed integers (UINT8: 0–255; INT8: −128 to 127), fixed-point representations, and floating-point scientific notation, explaining why standard formats such as FP32 (1,8,23 bits), FP16 (1,5,10), and BF16 (1,8,7) look the way they do. The key insight for ML is distributional alignment: neural network weights follow normal or Laplace distributions concentrated near zero, and floating-point formats naturally pack more representable values near zero — giving them an accuracy edge over uniform integer formats for a given bit-width.

Hardware efficiency tells the opposite story. An FP8 fused multiply-add (FMA) requires 40–50% more silicon area and energy than an INT8 FMA. Integer multiplication scales as n² in complexity while accumulation scales linearly; floating-point multiplication is cheaper but accumulation is expensive due to exponent alignment and normalization. This asymmetry drives the continued interest in INT8 inference despite floating-point's representational advantages.

The post surveys emerging formats: Log Number Systems (Nvidia proposal), NF4/AF4 lookup-table 4-bit formats for normally-distributed weights, PAL (Lemurian Labs, no commercial silicon yet), and block/microscaling formats that share exponents across element groups (Microsoft MSFP12, Nvidia VSQ, OCP Microscaling).

For inference the article reviews post-training quantization methods — simple rounding, LLM.int8() (outlier isolation), GPTQ (second-order weight information), SmoothQuant (activation outlier transfer), AWQ (activation-guided weight salience), QuIP, and AdaRound — noting that real-world performance losses tend to exceed what simple benchmarks suggest.

For training, Nvidia's FP8 recipe is detailed: all matmuls run FP8×FP8 with higher-precision accumulation; per-layer scale factors handle dramatically different tensor ranges; weight updates stay in FP32 because gradient magnitudes are tiny relative to weights; activation gradients can tolerate INT8 but weight gradients require at least FP8 (1,5,2) due to extreme outliers.

The article concludes that hardware designers face the challenge of specializing number formats without foreclosing future model architectures whose numerical distributions may look very different.

## Calls

No explicit ticker calls are made in this post. The piece is a technical educational deep-dive; Nvidia, AMD, Intel, Google, Microsoft, Meta, Arm, Qualcomm, MatX, and Lemurian Labs are mentioned as participants in quantization format development, but no directional views or price targets are expressed.
