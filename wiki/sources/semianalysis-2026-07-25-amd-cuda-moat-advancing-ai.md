---
type: source
title: "Can AMD break the CUDA Moat? AMD Advancing AI 2026"
tags: [amd, rocm, cuda, mi455x, helios, hbm4, serdes, tco]
related: ["[[semianalysis]]", "[[AMD]]", "[[AVGO]]", "[[NVDA]]", "[[CBRS]]", "[[META]]", "[[ai-accelerator-competition]]", "[[serdes-high-speed-connectivity]]", "[[hbm-memory]]", "[[advanced-packaging]]"]
created: 2026-07-28
updated: 2026-07-28
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/can-amd-break-the-cuda-moat-amd-advancing"
venue: SemiAnalysis
post_date: 2026-07-25
tickers: [AMD, AVGO, NVDA, CBRS]
---

# Can AMD break the CUDA Moat? AMD Advancing AI 2026

SemiAnalysis's third re-rating of AMD in a year: from "0% chance" of closing the CUDA gap →
"non-zero" (AMD 2.0) → now **a "great chance of success"** provided AMD solves two risks. Sentiment
context: they turned bullish when sentiment was at rock bottom. Lisa Su has leaned into an agentic
engineering culture; **Anthropic has publicly announced it will deploy 2GW of AMD chips**; Microsoft
reversed course and will deploy MI455X Helios (OpenAI likely the end customer via Azure); AMD is
doing a **Cerebras PD-disaggregation deal** for ultra-fast interactive inference (Groq-like).

**Silicon (Part 1):** MI455X is the most advanced chip out of a fab — first 2nm datacenter silicon
(N2 compute tiles + Venice CPU), largest CoWoS-L module at 5.5× reticle, only adopter of TSMC
SoIC-X hybrid bonding, 3,470mm² logic in-package, **12 HBM4 stacks = 432GB** (vs Nvidia/Google 8
stacks/288GB), 23.3 TB/s bandwidth. First chip with **active LSI** bridges. But AMD trails Nvidia
in microarchitecture — lacks Rubin's 3-bit LUT tensor cores — so it "spams silicon" to compensate.
**Helios rack:** 72 GPUs, 12 Broadcom Tomahawk-6 (102.4T) switches, first AMD switched scale-up.

**Two major risks:** (1) Helios rack **production-ramp hell** — no cableless tray design, and AMD's
weak SerDes means **up to 85% of the backplane must be retimed → 550+ Broadcom retimers per rack**
plus backplane reliability issues. (2) Chronic **internal GPU-cluster/CI shortage** blocking software
velocity; vLLM gating parity target for Advancing AI 2026 was missed and slipped toward Oct-2026.
Also: Meta's cut-down half-MI455 custom variant (4 dies / 6 HBM stacks) is bad for LLM work and
nukes AMD volume at Meta unless TBD Lab gets the full part.

**Economics (Part 3):** ~105% equity rebate structure for OpenAI/Meta (full rebate at AMD $600) makes
Helios cost-per-token "practically negative." Software still lands late and fragile (two-batch overlap,
WideEP, NIXL/RIXL upstreaming) but the ingredients are increasingly there. Net: still positive for
Nvidia ("the pie grows for everyone"; Rubin ships tokens at scale first), but AMD now a credible
share-taker.

## Calls
- [[AMD]] — **LONG** (px@call 494.95) — upgraded to "great chance" of cracking the CUDA moat; MI455X leads on silicon; risks are Helios ramp + CI cluster shortage.
- [[AVGO]] — **LONG** (px@call 383.22) — content winner off AMD's weak SerDes: 550+ retimers + 12 Tomahawk-6 switches per Helios rack.
- [[NVDA]] — **LONG** (px@call 196.51) — still leads; Rubin first to ship tokens at scale; has 3-bit LUT tensor cores AMD lacks.
- [[CBRS]] — **LONG** (px@call 188.61) — AMD-Cerebras PD-disaggregation inference deal validates the wafer-scale inference niche.
