---
type: source
title: "Culper Research vs Cerebras: A Neutral Engineering-Driven View"
tags: [cerebras, wafer-scale, electromigration, short-report]
related: ["[[irrationalanalysis]]", "[[CBRS]]", "[[foundry-process-node]]", "[[ai-accelerator-competition]]"]
created: 2026-10-29
updated: 2026-10-29
authors: [irrationalanalysis]
year: 2026
url: "https://irrationalanalysis.substack.com/p/culper-research-vs-cerebras-a-neutral"
venue: Irrational Analysis
post_date: 2026-10-28
tickers: [CBRS]
---
Irrational Analysis responds to the **Culper Research short report on Cerebras** (Oct-28), positioning itself as a "mostly neutral, activist investor" with a post-silicon-validation and lab-testing background (TSMC N5 — Cerebras's node — through N3P, Samsung 5LPP–SF3, Intel 18A).

**Core rebuttal — the physics:** Culper leans on an Arrhenius/electromigration model to allege Cerebras chips are run too hard. IA says this is "garbage, screams tourist": electromigration is driven by **temperature and current density, not raw power draw**, and the voltage bands / temperature limits / HTOL spec (5 vs 10 yr) / acceleration factors a designer targets at pre-silicon are **trade secrets** Culper cannot observe. You cannot compute reliability from power alone. Analogy: Meta runs Nvidia GPUs with dummy-FLOP load ("pytorch powerplantnoblowup" flag) to smooth grid draw — dummy load smooths power and thermals; there is "no practical difference" between dummy FLOPs (training) and Cerebras dummy tokens.

**Where Culper lands blows (IA concedes "fair points"):**
- The **OpenAI deal is fixed-price** and massively favors OpenAI; Cerebras failed to secure power/equipment, so rising power + datacenter costs hit it directly.
- **Power draw is critical for inference TCO** — running significant dummy load in *inference* (vs R&D training) murders product COGS. Structural economic disadvantage for wafer-scale.
- Cloud-model shift generates demand but also **hides hardware failure rates**.
- Thermal mismatch across the 84 WSE reticles comes from process variation, not just workload; mitigations (overvolt cold reticles, dummy energy-intensive ops) have limits.

**IA's own root-cause gut call:** not WSE warpage — more likely that in post-silicon validation Cerebras **juiced voltage / tuning registers** to fix functional/perf problems, pushing some subsystem past safe current density → the plausible cause of early CS-3 failures. "BallWire"/PariPoser interposer tech looks bad for power/signal integrity (ripple may have forced overvolt past +5%).

**Competitive threats to Cerebras (bigger than Etched):** Nvidia+Groq, AMD high-SRAM CPU + souped-up AVX-512 LPU-style, Google TPU + Marvell, OpenAI Jalapeño (no prefill-decode disagg).

**Verdict:** CS-4 is *supposed* to have much better thermals/power delivery; whether that fixes margins "we find out in ~6 months once CS-4 hardware gross margin flows through the financials." Given Cerebras's track record, IA is skeptical but genuinely neutral.

## Calls
- [[CBRS]] — **NEUTRAL** @ $119.31 — Culper's EM/Arrhenius analysis is wrong, but the fixed-price-deal + inference-power-TCO concerns are real; CS-4 gross margin the ~6-month tell. (Not the Oct-1 activist short; engineering-driven neutral.)
