---
type: source
title: "[V]ery [L]ong [I]ncoherent [W]riteup"
tags: []
related: []
created: 2024-02-24
updated: 2024-02-24
authors: [irrationalanalysis]
year: 2024
url: "https://irrationalanalysis.substack.com/p/very-long-incoherent-writeup"
venue: Irrational Analysis
post_date: 2024-02-24
tickers: [NVDA]
---

[[irrationalanalysis]] presents a detailed technical and historical critique of Groq's AI chip architecture, arguing it is a 144-wide Very Long Instruction Word (VLIW) design whose compiler is practically useless for third-party customers — a pattern repeated throughout 36 years of VLIW history.

The post opens with a primer on VLIW architecture: unlike CPUs and GPUs, VLIW removes on-chip scheduling logic (saving area and power) but places an enormous, often impossible burden on the compiler to statically schedule instructions into wide bundles. The author's core data point: a VLIW architecture with 8-wide bundles typically sees a compiler-generated average bundle occupancy of ~2 (25% utilization), rising to ~4-6 (50-75%) only after expert engineers spend weeks or months hand-writing assembly.

The author surveys non-Groq VLIW implementations — Intel Itanium (dead; bad compiler, killed by AMD64), Movidius/Intel Meteor Lake NPU (VLIW DSP core), AMD/Xilinx XDNA (DSP VLIW rebranded as 'Ryzen AI'), Qualcomm Hexagon (DSP VLIW rebranded as NPU), Google TPU (8-wide VLIW scalar unit, the only documented success), and Texas Instruments VelociTI. The pattern: every non-Google VLIW compiler has been effectively useless for third parties; Google is the sole exception but even TPU has seen almost no third-party traction.

The central thesis on Groq: Groq's architecture is 144-wide VLIW — 18x wider than Google's TPU — yet Groq's marketing avoids using the term 'VLIW' once in its 14-page whitepaper. First-party evidence from Groq's own marketing document reveals it took 5 days just to get the compiler to produce a functioning output for Llama-2 70B, yielding only 3.3% of optimal performance (1/30th). Groq's expert team then spent approximately 43 days hand-writing assembly to reach demo-quality numbers. The author argues this is standard VLIW failure — the compiler is practically useless, and no third-party customer will hand-code assembly for an exotic architecture. Groq's chief architect Dennis Abts quietly left for Nvidia in October 2022; the author notes a pattern of senior attrition, with many directors departing to form an ex-Groq startup called Positron AI.

The author introduces 'PPAP' (Power, Performance, Area, Pain) as an extension of the standard PPA framework — the fourth P being the pain inflicted on third-party developers, which VLIW maximizes. The conclusion: history does not favor a 144-wide VLIW succeeding where 8-wide designs have mostly failed.

## Calls

[[NVDA]] — MENTION — px@call n/a — Groq's chief architect defected to Nvidia and 'became filthy rich' on RSUs; framing implies GPU incumbents (NVDA) win as VLIW alternatives fail to gain third-party traction.
