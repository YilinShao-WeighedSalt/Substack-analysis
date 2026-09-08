---
type: source
title: "Hot Chips 2026: Irrational Recap"
tags: [hot-chips, hbm, hybrid-bonding, tpu, custom-asic, optics, cpu, cerebras]
related: ["[[irrationalanalysis]]", "[[BESI]]", "[[005930.KS]]", "[[CBRS]]", "[[NVDA]]", "[[GOOGL]]", "[[AMD]]", "[[INTC]]", "[[META]]", "[[MSFT]]", "[[AVGO]]", "[[MU]]", "[[LITE]]", "[[COHR]]", "[[hbm-memory]]", "[[advanced-packaging]]", "[[custom-silicon-asic]]", "[[silicon-photonics-interconnects]]", "[[ai-accelerator-competition]]"]
created: 2026-09-08
updated: 2026-09-08
authors: [irrationalanalysis]
year: 2026
url: "https://irrationalanalysis.substack.com/p/hot-chips-2026-irrational-recap"
venue: Irrational Analysis
post_date: 2026-09-06
tickers: [BESI, 005930.KS, CBRS, NVDA, GOOGL, AMD, INTC, META, MSFT, AVGO, MU, LITE, COHR]
---

# Hot Chips 2026: Irrational Recap

The author's engineering-first tour of Hot Chips 2026. The through-line: **the DRAM
giants overplayed their hand on HBM, and de-spec (12-hi → 8-hi/4-hi) is quietly
rewiring the packaging and memory theses.**

## Key arguments

- **HBM: "High-Bandwidth Mistake" vindicated.** All three DRAM makers presented
  defensively; the conference buzzed with **de-spec rumors** — customers want *fewer
  layers per stack* (still many stacks). Since 8-hi HBM does not need hybrid bonding,
  **hybrid bonding for HBM is "fucked"** — the author **liquidated his entire BESI
  position** and reallocated to EU/Japan optics ("RIP BESI lmao"). Expects we may
  never see 16-hi HBM. Future base dies improve by using real D2D PHYs (UCIe/NVLink/
  Broadcom MAX/Marvell 64G) and moving the controller off the main ASIC.
- **Samsung** showed the cleanest HBM base-die data — reason the author holds a
  **large long-only Samsung position**. Micron's deck "boring."
- **3D-DRAM electromigration risk** (D-Matrix Raptor, Cerebras, Nvidia/Groq, Fractile):
  server DRAM is rated ~80-85 °C but these run near logic temps; only HTOL testing
  proves reliability. D-Matrix is furthest along (first real 3D-DRAM test chips).
- **Cerebras**: activist SHORT reaffirmed — a 5-min chat with JP "confirmed the
  parametric-yield theory." Roasts JP's disagg "cables" strawman (GPU racks have
  cables too, and Cerebras will make money off GPU disagg). Deep-dive teased for Oct/Nov.
- **Custom ASIC**: **Meta MTIA** forced into a rec+genAI dual mandate = "worst of both
  worlds" (HBM permanently split for embedding cache) → more Nvidia revenue.
  **Microsoft Maia** "still dogshit" (8 pj/bit, 1 µs latency on N3P; hides real
  benchmarks). **Google TPU V8** shows real MoE progress (Boardfly 7-hop, NPO trial).
  **OpenAI Jalapeño** OOO cores are fascinating; but the SemiAnalysis-touted **25% B0-vs-A0
  perf/W jump is a RED FLAG** — signals a catastrophic A0 problem, not AI-design magic
  (Clive Chan + 10 engineers left post-tape-out).
- **Networking**: Nvidia **BlueField-4** beats Broadcom **Thor Ultra** on small-packet
  throughput; Spectrum-X multiplane praised.
- **GPU/CPU**: Nvidia **Rubin/Vera** solid (Vera fixes Grace's NoC + core flaws);
  **AMD MI400** rack "full of re-timers" (TCO/latency drag) but **Venice CPU** ~18.5%
  better than Vera. **Intel Xe** GPU "F-tier — put them out of their misery"; Diamond
  Rapids CPU finally adopts a central-IO die. **IBM dual-ISA Z+ARM** the coolest talk.
  Long roast of RISC-V ("nobody wants it").
- **Optics**: chat with AMS OSRAM's Ashkan — **Lumentum/Coherent are moving 850 nm →
  1060 nm VCSELs** (light passes through the substrate for bottom-emission density) but
  1060 nm needs new materials + a **6-12mo GR-468 requal** and un-characterized OM fiber;
  AMS OSRAM stays 850 nm and competes on packaging. A near-term speed bump for LITE/COHR
  in NPO/CPO.
- **Higher-level takes**: (1) **multi-vendor disagg inference is temporary** — only four
  compute entities matter (Nvidia, Google/TPU, Amazon/Trainium, AMD) and everyone goes
  vertical; Nvidia+Groq built a real rack-scale disagg product in 8 months. (2) AI
  chip-design acceleration is real (~5-10 yrs of EDA progress in 2-3 yrs) but **not a
  recursive singularity** — extrapolation cult debunked. (3) **DRAM vendors overplayed
  their hand** (>80% GM + shortage → buyers hunt every alternative).

## Calls

- **SHORT [[BESI]]** €202.50 (BESI.AS) — hybrid-bonding demand gutted by HBM de-spec; liquidated entire long.
- **LONG [[005930.KS]]** ₩274,250 — HBM base-die leadership; large long-only position held.
- **SHORT [[CBRS]]** $210.05 — parametric-yield thesis "confirmed"; activist campaign, deep-dive Oct/Nov.
- **LONG [[NVDA]]** $230.36 — owns half of CoWoS + most HBM at a discount; vertical integration wins the disagg era.
- **LONG [[GOOGL]]** $338.46 — TPU V8 real MoE progress; one of only 4 compute entities that matter.
- **NEUTRAL [[AMD]]** $477.57 — Venice CPU strong; MI400 rack re-timer TCO/latency drag.
- **NEUTRAL [[INTC]]** $95.80 — Xe GPU "F-tier"; Diamond Rapids CPU finally modernizes.
- **NEUTRAL [[META]]** $616.77 — MTIA dual-mandate "worst of both worlds" → more Nvidia revenue.
- **NEUTRAL [[MSFT]]** $499.70 — Maia "still dogshit," hides inference benchmarks.
- **NEUTRAL [[AVGO]]** $357.89 — Thor Ultra beaten by BlueField-4 on small-packet tput.
- **NEUTRAL [[MU]]** $1,016.59 — DRAM vendors "overplayed their hand"; boring HBM deck.
- **NEUTRAL [[LITE]]** $881.25 — 1060 nm VCSEL requal (GR-468, 6-12mo) + AMS OSRAM 850 nm competition.
- **NEUTRAL [[COHR]]** $281.86 — same 1060 nm requal headwind.
