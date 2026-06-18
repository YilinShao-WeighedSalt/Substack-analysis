---
type: overview
title: "Substack Investment Scan — Wiki Overview"
tags: []
related: []
created: 2026-06-17
updated: 2026-06-17
---

# Substack Investment Scan — Wiki Overview

## What This Wiki Is

This wiki is the persistent memory of the Substack Scanner routine, an automated agent that ingests semiconductor and AI-infrastructure analysis posts from five curated publications — Irrational Analysis, SemiAnalysis, Global Semi Research, Citrini Research, and Semi Doped — and organizes the findings into a browsable, interlinked markdown knowledge base.

Each ingested post becomes a `source` page: a structured summary with extracted investment calls, tickers, and links to the original article. Those calls flow up into `ticker` dossiers that track stance evolution and outcomes over time, `theme` pages that map narrative arcs across publications, and `publication` pages that score track records. `synthesis` pages capture cross-cutting conclusions — consensus positions, contrarian divergences, and sector-level reads. `query` pages flag open contradictions being watched. This overview sits at the root and is refreshed each run.

The wiki follows an append-only discipline: history is never rewritten. Corrections appear as dated notes. The index is the entry point; the agent reads it first and loads only the pages relevant to the current scan.

## Current High-Level Market Read (as of 2026-06-17)

The dominant theme across the most recent wave of posts is a battle for AI infrastructure primacy in which three hardware races are converging simultaneously: GPU compute, optical interconnects, and memory.

**Marvell's week.** The single biggest near-term event was Jensen Huang's endorsement of Marvell at Computex 2026 ("the next trillion-dollar company"), which sent MRVL up roughly 60-70% intraweek. Multiple publications covered this from different angles: Global Semi Research is straightforwardly bullish on Marvell's end-to-end data center portfolio (Teralynx switch at 102.4 Tbps, custom ASIC ramp, Celestial AI CPO acquisition); Semi Doped was present on the show floor and agrees the cross-sell between Marvell's ASIC and optical businesses is underappreciated; Irrational Analysis is more cautious — they exited the short but declined to buy, pointing to AMD CPU and Ciena as cleaner plays. Marvell's structural CXL card (Structera, pooling de-commissioned DDR4) is called out as an underappreciated, potentially 85%-gross-margin product.

**Co-packaged optics debate.** The hottest publication-level disagreement is whether CPO is on schedule. SemiAnalysis published a note arguing CPO deployments are materially delayed through 2027-2028; Global Semi Research published a direct rebuttal the same week, pointing to Nvidia's guidance to Coherent and Lumentum having jumped from ~40 million to ~100 million CW laser units between January and April/May 2026, and citing proprietary checks showing TSMC's COUPE ramp running ahead of schedule. The laser order surge is hard to reconcile with a genuine delay thesis. Near-term bridging solutions — "XPO" near-package optics and external-laser ELSFP modules — are emerging as pragmatic on-ramps before full CPO scale.

**Memory.** Irrational Analysis published a structural bear case on HBM as a long-term technology (TSV parasitics cap pin speeds; the end-state is clock-forwarded SerDes into co-packaged LPDDR over optical links) but a near-term bull case on DRAM broadly (agentic AI is a structural, non-pull-forward demand driver; another double or triple likely before a 70%+ peak drawdown). Their preferred play is Samsung (005930.KS) over Micron, citing Samsung's in-house logic foundry, silicon photonics CPO group, and co-design advantages on HBM PHY and optical I/O. Memory LTA structures (five-year contracts with 30% prepayments) are appearing — a signal that hyperscalers are locking in supply, which Global Semi Research reads as the market underestimating memory's long-cycle tightness.

**Intel.** SemiAnalysis made an explicit capital-raise call: Intel should issue roughly $25 billion in equity at the current valuation (richest since 2000) to fund the Terafab foundry program, anchored by SpaceX, Tesla, Google, and Nvidia. The board overhaul (Lip Bu Tan as CEO, ex-ASML and ex-Qualcomm directors) is seen as credibly technology-focused. Semi Doped highlighted Clearwater Forest's chiplet architecture (Intel 7 + Intel 3 + Intel 18A with EMIB and Foveros Direct 3D) as a maturing advanced-packaging story that could serve as a credible TSMC CoWoS alternative. The SMIC N+3 teardown (SemiAnalysis) showed China's Kirin 9030 Pro at TSMC N6-class density but with far greater process complexity, trailing current-generation SoCs by 2.7x — export controls are eroding at the node level but Intel's 18A retains a meaningful architectural edge.

**Power and 800VDC.** 800-volt DC power architectures appeared universally at Computex; silicon carbide handles grid-to-800V conversion, silicon handles the step-downs. Prefabricated AI infrastructure blocks (Vertiv, Delta, Schneider, Eaton) are cutting deployment timelines by roughly 50%. This theme intersects with the energy grid infrastructure plays (GEV, VRT, ETN, CEG) that have run hard but remain structurally supported by AI datacenter load growth.

**RL training infrastructure.** SemiAnalysis's most recent deep-dive frames RL training efficiency as a queue-health problem: generator (LLM inference), RL environment (sandbox), and trainer (gradient updates) must be throughput-matched. Four real case studies exposed recurring failure modes — curriculum mismatch, sandbox initialization limits at scale, tail-latency stragglers, and policy staleness from partial rollouts. NVDA H200 and GB300 are the incumbent hardware substrate; coding assistant ARR is on track to clear $100 billion by year-end, making RL infrastructure efficiency competitively critical.
