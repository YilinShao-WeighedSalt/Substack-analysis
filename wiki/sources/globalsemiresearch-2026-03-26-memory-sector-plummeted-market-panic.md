---
type: source
title: "The memory sector has plummeted, what is the market panicking about?"
tags: []
related: []
created: 2026-03-26
updated: 2026-03-26
authors: [globalsemiresearch]
year: 2026
url: "https://globalsemiresearch.substack.com/p/the-memory-sector-has-plummeted-what"
venue: Global Semi Research
post_date: 2026-03-26
tickers: [MU, 000660.KS, 005930.KS, 285A.T]
---

On March 26, 2026, the memory chip sector experienced a sharp pullback, with shares of Micron (MU), SK Hynix (000660.KS), Samsung Electronics (005930.KS), and Kioxia (285A.T) all declining sharply. [[globalsemiresearch]] argues the selloff was driven by a fundamental misreading of a year-old Google research paper — arXiv:2504.19874v1 — describing a KV cache compression algorithm called TurboQuant.

**What TurboQuant actually does.** TurboQuant is a vector quantization algorithm developed by Google Research that compresses KV Cache vectors during LLM inference from 32-bit floating point to approximately 3 bits, achieving roughly a 6x compression ratio while staying near the information-theoretic lower bound. It applies only to the KV Cache in the inference phase — a specific and bounded slice of AI memory usage.

**Three market misconceptions identified:**

1. **Scope error.** The market interpreted "6x compression" as a 6x reduction in total memory demand. In reality, TurboQuant touches only the KV Cache during inference. Model weights must be stored in full and cannot be compressed this way. Training workloads do not involve KV caches at all. Traditional data center applications are unaffected. The primary impact is on HBM; NAND Flash is barely touched.

2. **Latency vs. compression trade-off.** Higher compression ratios require more compute during decompression, adding latency. AI inference is extremely latency-sensitive — even tens of milliseconds of added delay degrades user experience materially. The author notes Google itself has not deployed TurboQuant at scale internally, precisely because of this trade-off in low-latency inference settings.

3. **Jevons Paradox ignored.** Even if KV cache compression matures, cheaper effective memory enables larger context windows (32K → 128K → 1M tokens), bigger batches, and more complex applications. Historical precedent in storage — larger hard drives filled up faster, cheaper DRAM led software to consume more — suggests total memory demand rises as efficiency improves, not falls.

The author concludes the selloff is disconnected from any real deterioration in memory supply/demand fundamentals, positioning it as a panic buying opportunity thesis for memory names.

## Calls

- [[MU]] — LONG — px@n/a — selloff misreads TurboQuant scope; real memory demand fundamentals intact
- [[000660.KS]] — LONG — px@n/a — SK Hynix dragged down by same misreading; HBM demand unaffected
- [[005930.KS]] — LONG — px@n/a — Samsung Electronics sold off on unfounded compression-demand fears
- [[285A.T]] — LONG — px@n/a — Kioxia decline unjustified; NAND barely impacted by KV cache algorithms
