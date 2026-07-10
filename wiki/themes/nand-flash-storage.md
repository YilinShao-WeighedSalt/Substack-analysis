---
type: theme
title: "NAND Flash & Storage"
tags: []
related: []
created: 2024-07-01
updated: 2026-07-10
status: maturing
first_seen: 2024-07-01
---
## Timeline
- 2024-07-01 — [[irrationalanalysis-2024-07-01-memory-is-still-commodity]] (irrationalanalysis)
- 2024-07-08 — [[irrationalanalysis-2024-07-08-nand-flash-hidden-ai-play]] (irrationalanalysis)
- 2024-07-08 — [[irrationalanalysis-2024-07-08-nand-flash-hidden-ai-play]] (irrationalanalysis)
- 2024-12-20 — [[irrationalanalysis-2024-12-20-marvell-broadcom-micron]] (irrationalanalysis)
- 2025-01-05 — [[irrationalanalysis-2025-01-05-long-mrdimm-short-nand-flash]] (irrationalanalysis)
- 2025-02-13 — [[irrationalanalysis-2025-02-13-high-bandwidth-flash-sandisk]] (irrationalanalysis)
- 2025-02-13 — [[irrationalanalysis-2025-02-13-high-bandwidth-flash-sandisk]] (irrationalanalysis)
- 2025-02-13 — [[irrationalanalysis-2025-02-13-high-bandwidth-flash-sandisk]] (irrationalanalysis)
- 2025-10-01 — [[irrationalanalysis-2025-10-01-partial-mea-culpa-sandisk-marvell]] (irrationalanalysis)
- 2026-01-13 — [[semianalysis-2026-01-13-interconnects-beyond-copper-cfet-nand]] (semianalysis)
- 2026-01-13 — [[semianalysis-2026-01-13-interconnects-beyond-copper-cfet-nand]] (semianalysis)
- 2026-03-05 — [[irrationalanalysis-2026-03-05-march-ms-tmt-madness]] (irrationalanalysis)
- 2026-03-05 — [[irrationalanalysis-2026-03-05-march-ms-tmt-madness]] (irrationalanalysis)
- 2026-05-04 — [[semidoped-2026-05-04-capex-memory-tax-deepseek-nand]] (semidoped)

- 2026-07-07 — [[globalsemiresearch-2026-07-07-molybdenum-vs-tungsten-nand]] (globalsemiresearch)
## Narrative
IrrationalAnalysis originated the NAND-as-AI-play thesis in mid-2024, arguing that flash storage was a overlooked beneficiary of AI infrastructure build-out while the market fixated on HBM and compute. The narrative turned more cautious by early 2025 when IrrationalAnalysis flipped to a "long MrDIMM, short NAND flash" posture, citing oversupply risk and the lack of a near-term structural demand catalyst comparable to HBM. The High Bandwidth Flash angle — focused on SanDisk and the potential for NAND to serve as a lower-cost memory-adjacent layer — emerged in February 2025 as the bull case evolved, though IrrationalAnalysis later issued a partial mea culpa on that trade by October 2025. SemiAnalysis entered the theme in early 2026 through a process and device lens, covering NAND alongside CFETs and advanced interconnects, while SemiDoped framed NAND's outlook through the lens of AI capex discipline and the DeepSeek efficiency shock. The theme has attracted steady but never dominant coverage, driven almost entirely by IrrationalAnalysis, suggesting a maturing debate around NAND's role in AI infrastructure rather than a breakout consensus call.

## Materials note — the molybdenum-for-tungsten word-line transition (added 2026-07-10)

**Plain language:** 3D NAND stores data by stacking memory cells vertically (now past **300 layers**); horizontal wires called **word-lines** address each cell. For 20 years those wires were **tungsten**. Past ~300 layers tungsten hits a wall: as wires thin, its resistance climbs and it needs a titanium-nitride *barrier layer* that eats conductor space; and it is deposited using **WF6** gas, whose released **fluorine** corrodes the insulation (voids/leakage). **Molybdenum** fixes both: >50% lower resistance in ultra-thin lines, *no* barrier layer needed (thinner layers, less wafer warping), and its precursor (molybdenum dichloride dioxide, MoO2Cl2) is **fluorine-free** so the corrosion problem vanishes. Kioxia's VLSI-2024 data showed ~1/25th the leakage failures of tungsten. All three NAND makers (Micron, Samsung, SK Hynix; Kioxia leading) now have it on production roadmaps, converting first lines in 2026.

**Why it matters as a theme:** "molybdenum is what lets NAND makers keep stacking, and stacking is the whole business model." Unlike the 2026 WF6 shortage (a *time-limited* China-export supply squeeze, relief ~mid-2027), this is a *durable, physics-driven technology transition*. Global Semi's investable angle is upstream — molybdenum **precursor** suppliers, **delivery hardware**, and the **qualification moat** (once a fab certifies a chemistry, switching is slow) — though a clean listed pure-play did not surface (specialty-chemical divisions / private players dominate). See [[semiconductor-specialty-gases]] and [[globalsemiresearch-2026-07-07-molybdenum-vs-tungsten-nand]].
