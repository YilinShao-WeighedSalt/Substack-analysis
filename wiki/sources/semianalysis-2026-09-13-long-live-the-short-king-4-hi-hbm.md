---
type: source
title: "Long Live the Short King: Why 4-hi HBM Wins"
tags: [hbm, memory, inference, packaging]
related: ["[[semianalysis]]", "[[MU]]", "[[000660.KS]]", "[[005930.KS]]", "[[hbm-memory]]", "[[advanced-packaging]]", "[[memory-dram-cycle]]"]
created: 2026-09-14
updated: 2026-09-14
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/long-live-the-short-king-why-4-hi"
venue: SemiAnalysis
post_date: 2026-09-13
tickers: [MU, 000660.KS, 005930.KS]
---

# Long Live the Short King: Why 4-hi HBM Wins

SemiAnalysis argues the years-long trend of ever-more HBM per accelerator has **broken**, and that **4-hi HBM is the optimal SKU for many inference workloads** from HBM4 onwards.

## The de-spec is real and deepening
- Rubin Ultra ships **192GB/GPU — down from 288GB** on standard Rubin and Blackwell Ultra (and vs an earlier 1TB expectation). 8-hi is becoming the new standard vs 12-hi today; not a year ago the industry expected 16-hi+.
- Driven partly by **HBM wafer scarcity** (not enough wafers to feed the N3 logic + CoWoS Nvidia secured) and rising HBM cost, but SemiAnalysis argues it's also architectural: extra capacity is often not worth the BOM.

## Why bandwidth beats capacity
- **Shorter stacks, same bandwidth:** a cube's 2048 I/Os are split across dies; 4-hi (512 I/O/die max) is the *lowest* stack that still harvests all 2048 I/Os → same bandwidth as 8-/12-hi. But cost scales with GB content → 4-hi is a much cheaper $/bandwidth ("almost a free lunch").
- Compute mix has shifted from **capacity-bound pre-training toward bandwidth-bound inference/RL decode**. Rack-scale worlds (GB300 NVL72 → 21TB aggregate HBM; Rubin Ultra NVL576) now hold model weights with huge headroom (Kimi K3 2.8T in MXFP4 = 1,561GB, <8% of NVL72), so the minimum-capacity threshold has dropped hard.
- **Roofline on Kimi K3 / NVL576:** at 105 tok/s/user 12-hi ≈ 8-hi throughput; at 213 tok/s/user no benefit beyond 4-hi. 8-hi gives only +8% peak throughput vs 4-hi, 12-hi +10% — but the **TCO premium is +12.1% (8-hi) / +26.3% (12-hi)** → taller stacks deliver *higher* cost/token at current memory prices.
- **KVCache offloading** to DDR DRAM relieves the capacity given up (a real InferenceX run with 85% vs 92% HBM util held throughput until concurrency >70). DeepSeek V4.1 Flash cuts active KVCache ~75%.
- Future-proofing counter: a 3×-Kimi-K3 model makes 8-hi worth it below 180 tok/s/user (not 12-hi) — but looped transformers (confirmed for GPT-6 Astra) scale by depth not weights, and labs' hardware teams (the loudest 4-hi advocates) will co-design models to fit.

## The new figure of merit: tokens/HBM-wafer
4-hi = ~2× the harvestable bandwidth per wafer vs 8-hi, ~3× vs 12-hi (better with higher 4-hi packaging yield). Moves the bottleneck off DRAM wafers onto logic/substrate/PCB/integration — and frees wafers back to starved conventional/server DRAM. Behind the paywall: framed as **win-win for memory-supplier profitability** (impact section truncated at paywall).

## Calls
- **[[MU]] — NEUTRAL @ $975.26.** De-spec caps HBM $-content growth per GPU (a headwind to the "ever-more-HBM" super-bull) but SA frames it win-win (frees DRAM wafers, raises tokens/wafer) → net wash.
- **[[000660.KS]] — NEUTRAL @ ₩1,718,000** (SK Hynix). Same read.
- **[[005930.KS]] — NEUTRAL @ ₩252,000** (Samsung). Same read.

Reinforces the HBM-de-spec / hybrid-bonding-collapse thread ([[irrationalanalysis]]'s BESI short): 8-hi and below need no hybrid bonding.
