---
type: source
title: "CapEx is just Memory Tax Now, Deepseek V4 NAND impact"
tags: []
related: []
created: 2026-05-04
updated: 2026-05-04
authors: [semidoped]
year: 2026
url: "https://www.semidoped.com/p/capex-is-just-memory-tax-now-deepseek"
venue: Semi Doped
post_date: 2026-05-04
tickers: [SNDK, MU, NVDA, AMD]
---
[[semidoped]] argues that hyperscaler capex has structurally decoupled from compute expansion: the ~$200B YoY increase from ~$500B (2025) to ~$700B (2026) is largely absorbed by rising memory and storage pricing rather than incremental flops, creating what the hosts call a "memory tax" with uncertain ROI for cloud providers.

**The memory tax thesis.** Microsoft explicitly attributed $25B of its $190B 2026 capex to higher component pricing. Meta similarly cited memory cost inflation as a driver of its capex raise. When capex funds supplier margin expansion rather than new capacity, hyperscalers gain pricing power in their own markets (AWS notes memory constraints are pushing enterprise workloads to the cloud), but the productive value of each dollar invested falls.

**SanDisk margin explosion.** The post's central bull case is SNDK. Revenue grew 97% QoQ and 251% YoY; gross margins expanded from 51.1% to 78.4% in one quarter, with guidance above 80% next quarter. The hosts attribute this entirely to pricing: capacity cannot scale within quarter timeframes. Five multi-year supply contracts are signed, three of which represent $42B in remaining performance obligations, locking in elevated pricing across hyperscaler buying cycles.

**DeepSeek V4 and SSD-centric inference.** DeepSeek's KV cache compression architecture enables "SSD-centric inference," shifting massive context storage from HBM to NAND flash. In agentic use cases, cache hit rates reach 95–99%, dramatically reducing per-token inference costs. A cited paper ("Dual Path: Breaking the Storage Bandwidth Bottleneck in LLM Inference") formalizes the architecture. The hosts argue this makes NAND flash structurally critical to inference economics — not just training storage — and validates SanDisk's positioning in the AI stack.

**HBM dynamics.** Samsung's memory revenue grew 101% YoY; its HBM market share recovered from a trough (~13–20%) toward competitive levels. The JEDEC HBM4 spec (8 Gbps/pin) is being exceeded by SK Hynix and Micron targeting 10–12 Gbps/pin for inference performance, making bandwidth-differentiated HBM non-fungible despite being nominally commodity. Micron CEO Sanjay Mehrotra is noted as SanDisk's co-founder (the company was originally named "SunDisk," renamed after Sun Microsystems trademark pressure).

**Custom silicon and accelerators.** Google's TPU is entering the merchant market at multi-gigawatt scale, with CoWoS/HBM allocation disclosed as a supply risk. AWS Trainium is at a $20B run rate with triple-digit growth; Trainium 2 is sold out and Trainium 3 nearly fully subscribed, with Jassy claiming tens of billions in annual capex savings vs. merchant chips. Meta has deployed ~1 GW of MTIA alongside a multi-vendor GPU strategy including AMD and Nvidia.

## Calls

- [[SNDK]] — LONG — n/a — multi-year supply contracts lock in elevated NAND pricing; SSD-centric inference thesis gives structural AI-era demand beyond training storage; gross margins expanding above 80%
- [[MU]] — MENTION — n/a — HBM3E/HBM4 bandwidth competition with SK Hynix; co-founder Sanjay Mehrotra's SanDisk origin cited as context for NAND sector history
- [[NVDA]] — MENTION — n/a — referenced as merchant GPU supplier facing custom ASIC displacement from hyperscaler in-house silicon programs
- [[AMD]] — MENTION — n/a — cited as part of Meta's multi-vendor GPU strategy alongside MTIA custom silicon
