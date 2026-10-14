---
type: source
title: "The Tragedy of 3D XPoint (AKA Intel Optane AKA Micron QuantX)"
tags: [memory, 3d-xpoint, pcm, dram, nand, intel, micron]
related: ["[[irrationalanalysis]]", "[[INTC]]", "[[MU]]", "[[nand-flash-storage]]", "[[memory-dram-cycle]]", "[[intel-foundry-decline]]"]
created: 2026-10-14
updated: 2026-10-14
authors: [irrationalanalysis]
year: 2026
url: "https://irrationalanalysis.substack.com/p/the-tragedy-of-3d-xpoint-aka-intel"
venue: Irrational Analysis
post_date: 2026-10-11
tickers: [INTC, MU]
---

A history/"shitpost" revisiting **3D XPoint (3DXP)** — Intel's *Optane* / Micron's *QuantX* — provoked by how "fucked" today's DRAM market is. 3DXP is phase-change memory (PCM) with performance **between NAND and DRAM**: byte-addressable, persistent, and DRAM-like in random-latency (100s× NAND on random latency, ~2–5× on a fair NVMe-vs-NVMe SSD comparison). Its real value was always **competing with DRAM** in latency/consistency/endurance-sensitive workloads (databases: SAP HANA, Oracle), *not* competing with NAND on cost-per-bit.

**Why it died (IA's read):** ~30% self-inflicted Intel execution, ~70% market conditions. Scaling stalled at **4 layers** while NAND marched 48→300+ layers; DRAM prices fell and squeezed 3DXP out of its natural DRAM-adjacent niche. The **interface killed it**: most 3DXP shipped as NVMe/PCIe SSDs (the "supersonic jet for 100-mile hops" — 8µs latency unacceptable) or as DC Persistent Memory in "Memory mode" (a dumb DRAM cache). Only **App-direct mode** (3DXP in DRAM slots, exposed to software with persistence — KV-cache/weights survive reboot) captured the real value, but it needed Optane-SKU CPUs + BIOS-level striping config, and Intel's **10nm/Ice Lake fiasco** meant using PMem sacrificed DRAM bandwidth. Zinsner (IA's "favorite CFO") helped kill it at *both* Micron and Intel; Micron sold the Lehi JV fab to TI for analog. Intel buried the write-off as a Q2-2022 non-GAAP footnote.

**The revival pitch:** IA argues CXL (a protocol on PCIe) could be the *right* bus for 3DXP/PCM, and the Chinese (Alibaba + Demingli) are reviving byte-addressable PCM for OCP 2026. 3DXP was "too early" for the AI era (KV-cache/weights persistence now matters) and "too late" to survive to today's vertical DRAM/NAND prices. Micron won't revisit (traumatized; DRAM prints money); Intel is "too busy" and Lip-Bu Tan is conservative. IA's one "degen hero" candidate: **SpaceX/Terafab licensing 3DXP from Intel** and cracking the >4-layer scaling Intel/Micron never did.

Educational core; secondary read-throughs rather than fresh high-conviction trades.

## Calls
- **[[INTC]] — NEUTRAL (constructive) @ $102.81.** Intel "finally back in its stride": **18AP is good** ("they fixed 18A with more time"), **EMIB-T advanced packaging going well** ("despite what the Taiwan degens keep screeching"), 14A activity (early), and the Products business ("which I considered a zero") "going to the moon because of agentic CPU revival." Would be the natural licensor if 3DXP revives.
- **[[MU]] — NEUTRAL @ $953.19.** DRAM prices "super high" — the whole premise for why 3DXP could pencil again — but Micron won't revive it (management "traumatized," and reviving a DRAM competitor is against self-interest; "just print more money expanding regular DRAM and HBM"). Reads as a supercycle-tightness datapoint, not a directional push.
