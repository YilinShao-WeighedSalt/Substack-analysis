---
type: ticker
title: "CBRS — Cerebras Systems"
tags: []
related: ["[[irrationalanalysis-2024-10-01-cerebras-s1-initial-analysis]]", "[[irrationalanalysis-2024-10-14-cerebras-cbrs-equity-report]]", "[[irrationalanalysis-2024-12-15-tenstorrent-state-ai-hardware-startups]]", "[[irrationalanalysis-2026-05-04-cerebras-cbrs-equity-research-2026]]", "[[semidoped-2026-05-15-cerebras-ipo]]", "[[irrationalanalysis-2026-06-24-cerebras-june-2026-earnings]]", "[[semidoped-2026-06-24-daily-update]]", "[[irrationalanalysis-2026-08-01-market-memo-a-tale-of-two-heroes]]", "[[irrationalanalysis-2026-08-09-cbrs-wolf-navitas-hbf]]", "[[semianalysis-2026-08-10-tilert-inferencex]]", "[[semidoped-2026-08-13-daily-update]]", "[[semidoped-2026-08-17-daily-update]]"]
created: 2024-10-01
updated: 2026-08-18
ticker: CBRS
current_stance: mixed
conviction: medium
last_review: 2026-08-18
---
## Call log
| date | publication | stance | px@call | thesis |
|------|-------------|--------|---------|--------|
| 2024-10-01 | [[irrationalanalysis]] | SHORT | n/a | Plan to ride IPO pop then short aggressively; 97% hardware revenue from one related party, poor gross margins, and overstated technical capabilities |
| 2024-10-14 | [[irrationalanalysis]] | SHORT | n/a | IPO is exit liquidity for insiders; G42 revenue concentration, dilutive option at $14.66/share, 36% gross margins, and inadequate compiler put company on path to irrelevance |
| 2024-12-15 | [[irrationalanalysis]] | SHORT | n/a | Judged comically overvalued relative to Tenstorrent; author plans to trade it bearishly post-IPO. |
| 2026-05-04 | [[irrationalanalysis]] | LONG | n/a | Wafer-scale architecture pivots from failed training ambition to defensible ultra-high-speed inference niche, validated by OpenAI $20B deal and AWS distribution |
| 2026-05-15 | [[semidoped]] | NEUTRAL | 185 | Wafer-scale inference chip with genuine engineering achievement but limited TAM and dual burden of chip design plus data center ops |
| 2026-06-24 | [[irrationalanalysis]] | LONG | 226.72 | Q1 beat but packaging yield (modeled 20%) caps margins at ~42%; activist campaign for WSE-4 FP8 and face-to-face I/O |
| 2026-06-24 | [[semidoped]] | NEUTRAL | 226.72 | Q1 revenue $193.4M (+94% YoY), guided $855–865M; shares fell 10% on margin disappointment; 88GB SRAM per rack limits large models |
| 2026-07-28 | [[semianalysis]] | LONG | 188.61 | AMD-Cerebras PD-disaggregation inference deal (Groq-like) validates the wafer-scale inference niche. |
| 2026-08-01 | [[irrationalanalysis]] | NEUTRAL | 198.71 | One share for an activist campaign; 'deserves a dedicated post' — coverage TBD. |

| 2026-08-09 | [[irrationalanalysis]] | SHORT | 234.76 | Activist campaign vs Feldman; WSE4 is 'gen 3.5' (power/clocks, not yield); suspects unsolved parametric yield caps final yield ~20%; covered-call short |
| 2026-08-10 | [[semianalysis]] | NEUTRAL | 234.76 | TileRT (persistent-kernel GPU software) reframes ultra-low-latency as a rentable 'speed tier' — structural pressure on specialist inference-ASIC TAM |
| 2026-08-13 | [[semidoped]] | NEUTRAL | 218.98 | Q2 miss, hardware revenue contracted QoQ, stock −17%; raised FY guide on inference-services mix. A datapoint for the yield-short / TAM-pressure bears |
| 2026-08-17 | [[semidoped]] | LONG | 251.98 | OpenAI Ultrafast GPT-5.6 "Sol" live on Cerebras wafer-scale (14x); commercial win outside Nvidia; cloud rev +287% |

## Thesis evolution
irrationalanalysis opened with a consistently bearish view across three calls spanning late 2024, citing fatal customer concentration (G42 as near-sole buyer), structurally weak gross margins around 36%, and a wafer-scale architecture it viewed as technically overblown. By mid-2026 the same publication reversed to bullish after Cerebras secured an OpenAI $20B inference deal and AWS distribution, arguing the company found a defensible niche in ultra-low-latency inference where wafer-scale die actually delivers differentiated speed. The June 2026 earnings call reinforced the LONG: despite calling the transcript a "trainwreck," irrationalanalysis deepened its conviction by modeling the packaging yield problem (20% estimated) as the central financial variable — improvement from 20% to 50% would lift gross margins from ~42% to ~72%. The author initiated a symbolic "activist campaign" focused on three catalysts: WSE-4 with FP8 support, face-to-face I/O to solve KV cache offload, and a packaging yield investor day. semidoped maintained NEUTRAL at first earnings, noting shares fell 10% despite the beat and flagging the 88GB SRAM-per-rack constraint for large models. The two publications continue to disagree on conviction — irrationalanalysis sees solvable engineering bottlenecks, semidoped sees structural TAM and business model risks.

## Outcome tracking
semidoped's NEUTRAL at $185 IPO is now tracking wrong — stock at $226.72 (+22.6%) ✗ for the cautious positioning. irrationalanalysis's June 2026 LONG at $226.72 and semidoped's June 2026 NEUTRAL at $226.72 are both open (< 30 days). The three 2024 SHORT calls have no px@call and cannot be scored. Q1 2026 earnings ($193.4M revenue, $855–865M guide) beat estimates, partially validating the revenue diversification beyond G42, though shares fell 10% on margin concerns. The view would be falsified bearishly if packaging yield fails to improve above 30%, WSE-4 ships without FP8 support, or the OpenAI deal proves non-recurring.

**Update 2026-07-28:** SemiAnalysis flags an **AMD-Cerebras PD-disaggregation deal** (Cerebras wafer-scale for ultra-fast interactive decode alongside AMD GPUs), a Groq-Nvidia-style arrangement that validates the inference-niche pivot. New LONG at $188.61. But the tape is brutal: irrationalanalysis's Jun-24 LONG at $226.72 has now **resolved at $188.61, -16.8% → LOSS** (>30d); semidoped's Jun-24 NEUTRAL at $226.72 (excluded) looks prescient. CBRS is ~51% off its 52-wk high. Deal is a real catalyst but does not fix the margin/packaging-yield overhang.

**Update 2026-08-12:** a genuine three-way split now sits on CBRS. (1) SemiAnalysis's Jul-25 LONG ($188.61) is **+24.5% ✓ (open)** — the AMD PD-disagg deal thesis is working on the tape. (2) IA reiterates an activist SHORT ($234.76), arguing WSE4 is a 'gen 3.5' power/clock refresh and that Feldman's 'doubling clocks' brag betrays an *unsolved parametric-yield* problem (final yield ~20%). (3) SemiAnalysis's OWN new TileRT note ($234.76 NEUTRAL) is structurally cautionary on the inference-ASIC TAM Cerebras depends on. Bull tape vs bear fundamentals — see [[cbrs-yield-short-vs-inference-tam]].

**Update 2026-08-15:** SD NEUTRAL $218.98 (Aug-13). Cerebras missed and fell ~17%, with **hardware revenue contracting QoQ** — a concrete datapoint on the bear side of [[cbrs-yield-short-vs-inference-tam]] (IA's parametric-yield activist short + SA's own TileRT TAM-pressure note). CBRS raised FY guide on inference-services mix, shifting away from hardware. IA's Aug-9 SHORT ($234.76) is +6.7% (short working, open). The SA Jul-25 LONG ($188.61, +16.1%) remains the bull counter, open, resolves ~Aug-24.

**Update 2026-08-18:** OpenAI ships **Ultrafast GPT-5.6 "Sol" on Cerebras** wafer-scale (14x speed) — a live commercial inference win *outside* Nvidia's stack; cloud rev +287%. CBRS +19% on Aug-17 to $251.98. This lands squarely on the bull side of [[cbrs-yield-short-vs-inference-tam]]: SA's Jul-25 LONG ($188.61) is now **+33.6%** (open, resolves ~Aug-24), while **IA's Aug-9 activist SHORT ($234.76) has flipped to -7.3% underwater**. The momentum that cooled toward the bears last run (the Aug-13 miss) swings back to the tape. New SD Aug-17 LONG $251.98.
