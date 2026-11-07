---
type: source
title: "IA: Avicena Deep-Dive — uLED vs Credo's uVCSEL for slow-and-wide scale-in"
tags: []
related: ["[[CRDO]]", "[[AVGO]]", "[[MRVL]]", "[[LITE]]", "[[TSM]]", "[[silicon-photonics-interconnects]]", "[[co-packaged-optics]]", "[[irrationalanalysis]]"]
created: 2026-11-07
updated: 2026-11-07
authors: [irrationalanalysis]
year: 2026
url: "https://irrationalanalysis.substack.com/p/avicena-deep-dive"
venue: Irrational Analysis
post_date: 2026-11-06
tickers: [CRDO, AVGO, MRVL, LITE, TSM]
---

A 9k-word engineering deep-dive on **Avicena** (private microLED optical-interconnect startup, "LightBundle"). Avicena uses GaN microLEDs grown on their own wafer then die-to-wafer-attached to a **TSMC N12** logic die, with simple **clock-forwarded 2-4G** links (no CDR/ADC/DSP) — far simpler than a transceiver, and much easier than Nvidia's 32G D2D. Roadmap: silicon PDs co-designed with TSMC (up to ~10dB gain → cut drive current to ~0.5mA/LED), and "IO-squared" **direct-drive LEDs printed onto a leading-edge logic wafer (N3P)** — the holy grail. First product: a **1.6T gearboxed slow-and-wide AOC targeting 10m** reach. IA's verdict moved from "Credo/uVCSEL will vaporize you" to "maybe they have a chance to be cost competitive" — but the catch is **fibers**: Avicena needs ~**6x the fibers** of a Credo/uVCSEL 1.6T AOC, and OM-fiber cost is the swing factor. Reach map: <=5m served by copper AEC (Credo/[[AVGO]]/[[MRVL]], all rumored failing at 6m); uVCSEL scales to 20-30m; **Avicena must hit 10m to be commercially viable** — if it only reaches 7m, Credo "will just scale, bundle, and cross-sell." Everyone (incl. IA) will request samples H2-2027 at 1K/10K/100K/1M pricing and find out.

## Calls
- **[[CRDO]] LONG (reaffirm)** — uVCSEL slow-and-wide is the winning scale-in path; Avicena has only a narrow 10m window + ~6x fiber-cost penalty.
- Context: **[[AVGO]]/[[MRVL]]** copper AEC (<=5m), **[[TSM]]** as Avicena's N12/N3P partner, **[[LITE]]** optics.
