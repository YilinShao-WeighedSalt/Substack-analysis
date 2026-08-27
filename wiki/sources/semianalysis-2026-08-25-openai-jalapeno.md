---
type: source
title: "OpenAI Jalapeño: Better Than Nvidia Blackwell"
tags: [custom-silicon, inference-asic, hot-chips-2026, hbm4]
related: ["[[semianalysis]]", "[[AVGO]]", "[[NVDA]]", "[[AMD]]", "[[CBRS]]", "[[005930.KS]]", "[[custom-silicon-asic]]", "[[ai-accelerator-competition]]", "[[hbm-memory]]", "[[eda-chip-design]]"]
created: 2026-08-27
updated: 2026-08-27
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/openai-jalapeno-better-than-nvidia"
venue: SemiAnalysis
post_date: 2026-08-25
tickers: [AVGO, NVDA, AMD, CBRS, 005930.KS]
---

# OpenAI Jalapeño: Better Than Nvidia Blackwell

SemiAnalysis was invited into OpenAI's lab to run its **InferenceX** suite on **Jalapeño**, OpenAI's first custom inference ASIC (unveiled with [[AVGO|Broadcom]] on June 24). Headline: Jalapeño **beats every Nvidia, AMD and Google chip SemiAnalysis has tested on tokens per All-in-utility MW**, across nearly the whole latency curve — and does it with single-token prediction, no speculative decoding, and **no prefill-decode disaggregation (PDD)**.

## Key facts
- **Timeline:** design began mid-2024; CoWoS tape-out Nov 2025; A0 results after ~3 months bring-up; ~16 months hiring-to-tapeout (OpenAI cites 9 months initial-design-to-tape-out). An "insane" ASIC cadence — validates AI-accelerated EDA (claimed 8% SIMD / 10% matrix-engine area reduction from AI-assisted design).
- **Silicon:** B0 stepping in fab, ~25% better perf/W: **13.4 PFLOPs MXFP4** on a reticle-sized **N3P** die at 700 W (vs Rubin compute die ~17.5 PFLOPs dense NVFP4 at 900–1,150 W). **HBM4 at 15.4 TB/s/package (~10 Gbps pin > Rubin's 9.6)** — SemiAnalysis believes **stacks are Samsung's** ([[005930.KS]]).
- **Perf:** >700 tok/s/user at concurrency 1 on DeepSeek R1; Kimi-K2.5 / GPT-OSS ~1,400 tok/s/user. Kernels written with **Codex** in OpenAI's Gluon language (Triton-based, Linear Layouts algebra); serving engine "Teacup"; simulator "chilisim" ±5%.
- **System:** 128 Jalapeño/rack (16 "Vindaloo" trays) + AMD EPYC Turin host rack ("Katsu") + Broadcom **Tomahawk-6** scale-up switches ("Chana"); scale-up to **2,048 chips** over 16 racks via copper backplane + 1.6T optics + OCS. ~160 kW / two-rack system. System integration by **Celestica**.
- **Architecture:** weight-stationary systolic (TPU-like) but small-shape friendly; out-of-order cores with L1 (unusual vs scratchpad accelerators); minimal NoC/memory hierarchy; skips PDD to keep a fungible fleet (avoids stranding chips as traffic mix moves).

## Caveats (SemiAnalysis' own)
- All numbers OpenAI-supplied; verified in person only on 8k/1k, **no AgentX long-context results yet**.
- Fair comparison is **Rubin (also HBM4), not Blackwell** — and **Rubin ships to customers now** while Jalapeño is engineering samples. Production ramps through 2027, most volume late next year.
- Models tested (R1, Kimi K2.5, GPT-OSS) are not on the open frontier (vs DeepSeek V4 Pro / Kimi K3).

## Calls
- **[[AVGO]] LONG $355.59** — Jalapeño's ASIC partner + Tomahawk-6 scale-up switches; the biggest merchant beneficiary of the custom-silicon wave.
- **[[NVDA]] NEUTRAL $209.66** — real threat to DC gross margins (CNBC framing), but Rubin ships now and leads on the fair comparison; moat pressured, not breached.
- **[[AMD]] NEUTRAL $480.93** — EPYC Turin hosts every Jalapeño rack, but SemiAnalysis says "AMD's kernel team should be worried."
- **[[CBRS]] NEUTRAL $182.15** — SemiAnalysis' read: Cerebras' 1.25 GW option beyond OpenAI's firm 750 MW is "now in question."
- **[[005930.KS]] LONG ₩265,000** — believed near-exclusive HBM4 supplier for Jalapeño.
