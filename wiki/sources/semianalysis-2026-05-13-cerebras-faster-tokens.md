---
type: source
title: "Cerebras — Faster Tokens Please"
tags: []
related: []
created: 2026-05-13
updated: 2026-05-13
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/cerebras-faster-tokens-please"
venue: SemiAnalysis
post_date: 2026-05-13
tickers: [NVDA, AMD, VICR, TSM]
---

[[semianalysis]] delivers a deep technical and financial dissection of Cerebras's wafer-scale inference business, covering the OpenAI and AWS partnerships, the tokenomics of fast inference, WSE-3 architecture, datacenter ramp, and technical roadmap.

## Fast Inference as a Business

The piece opens with the argument that tokens-per-second has become a genuine competitive differentiator — users demonstrably pay premiums for interactivity. Anthropic's Opus 4.6 fast mode commands 6x pricing for 2.5x interactivity (currently delivering ~1.75x speed at ~70 tps vs. ~40 tps standard). Cerebras's WSE-3 wafer-scale engine can reach thousands of tokens per second on smaller models by virtue of its 21 petabyte/s on-chip SRAM bandwidth — versus HBM-based GPUs constrained by off-die memory bandwidth at decode time.

## OpenAI Deal Structure

The financial terms are substantial: a 750MW committed capacity purchase spanning 2026–2028 representing $24.6B in remaining performance obligations, an optional 1.25GW expansion tranche, a $1B working capital loan at 6% interest (waived if repaid via capacity delivery), and a warrant grant worth up to ~$2.74B (~33.4M shares at $82.02 grant value, exercise price effectively $0). The warrant contra-revenue treatment and vesting triggers (including a $40B Cerebras market-cap threshold) create complex incentive structures tying OpenAI's economics to Cerebras's valuation trajectory.

## WSE-3 Architecture Strengths and Ceilings

The WSE-3 is fabricated on TSMC N5 with 44GB of on-chip SRAM (50% of silicon area), 900,000 enabled compute cores, 25kW power draw, and 21PB/s internal bandwidth. It excels at low arithmetic-intensity decode workloads. However, three structural ceilings bind it: (1) SRAM capacity has essentially stopped scaling — WSE-1 at 18GB (16nm), WSE-2 at 40GB (7nm), WSE-3 at 44GB (5nm), with N3E offering near-zero shrink going forward; (2) off-wafer I/O bandwidth is severely constrained at 150GB/s by the wafer's edge geometry, versus 900GB/s NVLink5 per GPU and 9.6Tb/s for Groq LP30; (3) fitting any model larger than ~120–355B parameters requires pipeline parallelism that undermines the wafer's latency advantage.

## Real-World Workload Mismatch

Analysis of 432,000 real agentic requests shows median input sequence length of 96.3k tokens, with nearly 50% exceeding 128k — a regime that stresses Cerebras's context-length and multi-wafer parallelism strategy. Against a single Blackwell Ultra with 288GB HBM3E (6.5x Cerebras's SRAM), or an NVL72 rack with 20–100x aggregate throughput at lower interactivity levels, Cerebras wins only in the narrow band of small-model, short-context, latency-critical inference.

## BOM and Competitive Context

The CS-3 system BOM is estimated at $450k/rack (up from $350k pre-Q4 memory price hike), incorporating 84 Vicor power bricks, 12 Xilinx 100GbE FPGAs, and a dual-socket AMD CPU node with 6TB DDR5 for KV cache offload. The article contrasts Cerebras's "moonshot R&D" capital allocation (hybrid-bonded DRAM wafer, Ranovus photonic interconnect) against AMD's $221M/quarter buyback program, framing the latter as misallocated capital.

## Calls

- [[NVDA]] — LONG — px@n/a — Dominant incumbent with 20–100x throughput advantage at scale; acquired Groq in December 2025, consolidating SRAM-accelerator competition
- [[AMD]] — MENTION — px@n/a — Mentioned for GPU competition and criticized for prioritizing buybacks ($221M/quarter) over R&D investment in next-generation inference silicon
- [[VICR]] — MENTION — px@n/a — Significant BOM content supplier (84 Vicor power bricks per CS-3 system); benefits from Cerebras datacenter ramp
- [[TSM]] — MENTION — px@n/a — Fabricates WSE-3 on N5; wafer loadings step up materially each quarter through 2026–2028 to meet OpenAI deployment schedule
