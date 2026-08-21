---
type: source
title: "Cerebras's Next Generation CS-4: Fast Just Got Faster"
tags: [cerebras, wafer-scale, inference, cs-4, disaggregated-inference, tilert]
related: ["[[semianalysis]]", "[[CBRS]]", "[[cbrs-yield-short-vs-inference-tam]]", "[[ai-accelerator-competition]]", "[[semianalysis-2026-08-10-tilert-inferencex]]"]
created: 2026-08-21
updated: 2026-08-21
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/cerebrass-next-generation-cs-4-fast"
venue: SemiAnalysis
post_date: 2026-08-19
tickers: [CBRS]
---

Technical teardown of CS-4, Cerebras's 4th-gen rack around the **same 5nm WSE-3**. CS-4 doubles CS-3 performance by **doubling clock speed** (fed by dramatically more power + better delivery/cooling), lifting off-wafer I/O to **2.4 Tb/s** (from 1.2), peak FLOPs, and — the metric that matters — **~2x memory bandwidth → ~2x tokens/sec/user**. Unchanged: **44 GB SRAM/wafer** (bit-cell limited), the architecture's core low-memory tradeoff.

**Backpack rack:** split into front power / rear compute "backpacks," **3 wafers/rack** (up from 2); cooling moved out (datacenters now fully liquid-cooled). Simpler to manufacture; effective BOM/wafer could match CS-3 → **near-2x interactivity/token-revenue at similar TCO** — "a no-brainer for customers." Field-upgradeable **Wafer I/O** module (FPGA NIC → standard ethernet) enables **disaggregated inference** (pair CS-4 with HBM XPUs to cover low SRAM; AWS EFA/Trainium in mind).

**SemiAnalysis's caveats:** power/rack is **125-135kW** (~2x CS-3's 23kW×... ), so **perf/W is at best a slight improvement**; the "2,000x more BW than Rubin" marketing yields a real ~20-40x interactivity claim they accept as fair, but the **3µs fat-tree latency** (down from 5µs; ns for some rivals) still **blocks EP/ETP across wafers**, forcing pipeline parallelism. Explicitly ties back to their **TileRT** note (GPU high-interactivity "speed tier"). Overall: a real but **modest** systems iteration.

## Calls
- [[CBRS]] — **NEUTRAL** @ $209.85 — CS-4 doubles interactivity at similar TCO (attractive) but is a same-silicon power/clock/systems iteration with only slight perf/W gain; 3µs net still a bottleneck vs ns-class rivals and TileRT-style GPU software.
