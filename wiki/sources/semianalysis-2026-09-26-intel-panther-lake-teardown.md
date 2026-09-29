---
type: source
title: "SemiAnalysis — Intel Panther Lake Teardown"
tags: [intel-18a, backside-power, gaa, ribbonfet, foveros, teardown]
related: ["[[semianalysis]]", "[[INTC]]", "[[TSM]]", "[[005930.KS]]", "[[foundry-process-node]]", "[[advanced-packaging]]", "[[advanced-transistor-materials]]", "[[intel-foundry-decline]]", "[[semiconductor-equipment]]"]
created: 2026-09-29
updated: 2026-09-29
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/intel-panther-lake-teardown"
venue: SemiAnalysis
post_date: 2026-09-26
tickers: [INTC, TSM, 005930.KS]
---

# SemiAnalysis — Intel Panther Lake Teardown

STEEL-lab physical teardown of Intel's Core Ultra 7 365 (Panther Lake), the first product on Intel 18A. Paywalled; full body served. A milestone read, not a priced thesis.

## Summary

**The milestone (real):** Panther Lake is the **first commercial implementation of backside power delivery** (Intel's "PowerVia"/BSPDN), Intel's **first RibbonFET (GAA) transistors**, and showcases **Foveros-S** 2.5D packaging. Intel's manufacturing arc has moved "from nebulous roadmaps to shipped silicon."

**The limit (measured):** SemiAnalysis's own measurements put **18A compute-logic density on par with TSMC N3E** (an older node) — and **18A does NOT lead TSMC N3P, N2, or Samsung SF2 on peak density.** Package structure underlines the caution: the **compute tile is 18A**, but the **high-end 12-core GPU tile is still TSMC N3E** (smaller GT1 GPU on Intel 3; I/O tiles on TSMC N6). So the leading-edge node is confined to the compute tile; graphics/I-O ride cheaper, established processes.

**Technical color (feeds themes):**
- **PowerVia** routes power on a backside BM0–BM5 stack through Mo-lined W nano-TSVs to local S/D contacts; recovers less cell area than a direct backside contact but frees frontside routing. 18A uses a **five-track logic library** (vs 7-track on N3E/Intel 3); PowerVia lets Intel pair a compact cell height with wider, lower-resistance M0.
- **RibbonFET** stacks **four** silicon nanosheets (vs Samsung SF2 MBCFET's **three**); dipole (La) threshold tuning, TiAl (NMOS)/TiN (PMOS) work-function metals, W fill; full dielectric subfin isolation (enabled by BSPD) cuts parasitic capacitance but weakens the thermal path.
- **Materials/equipment cues:** Mo replaces TiN liners for W contacts; Nb barriers at coarse metals; Co/Ru at fine metals; **Applied Materials' Endura** thermal-wetting for void-free Cu fill; **Lam Research** molybdenum metallization; **Synopsys** DDR-PHY firmware referenced. NPU 5 shrinks 36.9% (consolidated MACs, native FP8). Wildcat Lake (Apr-2026) is the value 18A variant using UCIe (Intel's first).
- **Recovery framing:** Intel took GAA + BSPD on at once; a sustained lead now depends on product perf, cost, yield, and the next 18A implementation. It "does not hold the process-technology leadership it held prior to 10nm."

## Calls
- [[INTC]] — NEUTRAL — $123.00 — 18A is a genuine manufacturing milestone (first BSPD + first RibbonFET + Foveros-S, shipped), but density only matches TSMC N3E and trails N3P/N2/SF2; the high-end GPU tile is still TSMC N3E. Milestone confirmed, not process leadership → catalyst for foundry credibility, not (yet) a re-rate.
- [[TSM]] — thesis-reinforcing (no separate priced call this post) — still wins Panther Lake's GPU (N3E) + I/O (N6) tiles and leads on peak density (N2/N3P).
- [[005930.KS]] — thesis-reinforcing — SF2 MBCFET (3-sheet, no BSPD) is the GAA reference point; full SF2 teardown promised.
