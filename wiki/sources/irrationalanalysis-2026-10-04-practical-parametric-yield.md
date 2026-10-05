---
type: source
title: "Practical Parametric Yield (Featuring Cerebras)"
tags: [parametric-yield, cerebras, wafer-scale, jalapeno, binning]
related: ["[[irrationalanalysis]]", "[[CBRS]]", "[[AVGO]]", "[[foundry-process-node]]", "[[ai-accelerator-competition]]", "[[cbrs-yield-short-vs-inference-tam]]", "[[jalapeno-parametric-yield-vs-benchmarks]]"]
created: 2026-10-05
updated: 2026-10-05
authors: [irrationalanalysis]
year: 2026
url: "https://irrationalanalysis.substack.com/p/practical-parametric-yield"
venue: Irrational Analysis
post_date: 2026-10-04
tickers: [CBRS, AVGO]
---

# Practical Parametric Yield (Featuring Cerebras)

The long-teased **parametric-yield deep-dive** (promised since the Aug/Sep activist-short notes), re-written around Cerebras. The author argues parametric yield is "the only thing that matters for the next 12–18 months" for [[CBRS]].

## Plain-language core
- **Parametric yield** = the fraction of chips that meet target clock/power *after* catastrophically-defective dies are already scrapped. It is an **economic choice** (where on the volt/freq curve you ship), not a design choice; post-silicon validation measures reality and product management sets the SKU clocks.
- The physical world is **Gaussian**: transistor threshold, leakage, rise time all vary. Designers margin at ±2σ process / ±10% voltage; a characterization lot maps the corners a-priori; HVM then "throws darts blindfolded." Expected parametric yield when everyone does their job ≈ **95%**.
- Everyone else manages it three ways: (1) **scrap** too-slow/too-hot dies, (2) **harvest** them as cheaper SKUs (AMD Turin 9575F vs 9535; Nvidia "Ti/Super" bins), (3) **tune registers/voltages** per chip. Testing is cheap at die level (socketed rigs, thermal heads).
- **"Be first, be smarter, or cheat."** Semis are self-policed; cheating (cherry-picking TT parts, unsafe undervolt claims, debug registers that juice perf but cause electromigration) is easy and only caught by independent volume testing. Reputation is the enforcement mechanism.

## Cerebras is disproportionately hurt (not their fault)
- Wafer-scale = **84 reticles fused on one wafer** with a (suspected) **unified power grid**. Cerebras **can't scrap, can't harvest, can't easily socket-test** — it must package the whole wafer with bespoke vertical power + cooling before it can be fully characterized. A failed packaged wafer is catastrophic vs tossing 1–2 reticle dies.
- Author's read: parametric yield got the *least* attention of Cerebras's ~10 existential problems; Sean/JP "only just started to seriously look at it." CS-4/WSE3-turbo **doubled all clocks on the same silicon** — consistent with having been stuck in a hilariously low part of the volt/freq curve, now unlocked by better cooling + reduced supply-ripple.

## The call — a *softening*, not a reaffirmed short
- **CBRS NEUTRAL $166.43.** CS-4 enclosure = "**great progress**," product-level yield "**significantly better**," **financials/GM inflection likely H1 2027** (supply-limited today as CS-4 ramps). WSE4 has many vectors: split power grids for per-reticle voltage, DVFS, decoupled compute/SRAM/NoC clocks, PVT-tolerant custom cells. Markedly less bearish than the Oct-1 activist SHORT.

## Jalapeño side-swipe (→ contradiction with SemiAnalysis)
- SemiAnalysis reported OpenAI **Jalapeño** (TSMC N3P, Broadcom co-design) had a **25% A0→B0 perf/watt delta**. Author: "an absolutely massive red flag on fire" — a 25% shift after characterization means **catastrophic parametric-yield failure** (5–10% = modest mistake, 15% = severe, 25% ≈ disaster). "A0 is broken." Blames either Broadcom or OpenAI's "AI-vibe-coded RTL." Opposite conclusion to SA's bullish Jalapeño piece → see [[jalapeno-parametric-yield-vs-benchmarks]].

## Calls
- **[[CBRS]] NEUTRAL** $166.43 — parametric-yield deep-dive; structural wafer-scale disadvantage on binning/harvest/test, but CS-4 power/cooling progress → possible H1-27 margin inflection. Softens the activist short.
- **[[AVGO]] (context, no stock call)** — Jalapeño 25% A0→B0 delta flagged as a parametric-yield "disaster" on a Broadcom-co-designed, N3P chip; execution-risk datapoint, not a directional AVGO call.
