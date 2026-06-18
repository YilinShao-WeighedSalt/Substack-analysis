---
type: source
title: "Practical Optical Communication Systems"
tags: []
related: []
created: 2025-11-07
updated: 2025-11-07
authors: [irrationalanalysis]
year: 2025
url: "https://irrationalanalysis.substack.com/p/practical-optical-communication-systems"
venue: Irrational Analysis
post_date: 2025-11-07
tickers: [LITE, COHR, GFS, KEYS]
---

[[irrationalanalysis]] walks through the practical engineering hell of optical communication systems — contrasting the near-ideal channel properties of fiber with the satanic complexity of everything else in the stack: tuning, filters, modulation, reliability, and electronics integration.

**Tuning.** Electronic circuits offer rich, granular tuning options (8-bit Vdd adjustment, varactors, multi-transistor bias). Photonic structures are tuned almost exclusively with tiny resistive heaters, yielding near-zero granularity. This forces essentially every photonic parameter into closed-loop PID control — a debugging nightmare because adjusting one control loop disturbs neighboring structures through thermal crosstalk.

**Filters.** Photonic filters (rings, MZIs) have terrible insertion loss, poor rejection ratios, and — critically — perfectly periodic responses. Electronic filters are not periodic. This periodicity creates fundamental design constraints with no electronic analog.

**Modulation.** Optical modulators require 2+ V swing; high-speed SerDes tops out at ~1200 mV. This forces a discrete driver amplifier into every optical link — adding noise, cost, and packaging complexity. On the receive side, photodiodes produce weak output that requires powerful TIAs, which are similarly noisy and expensive. These are necessary evils, not solved problems.

**Modulator tier list.** For pluggable 1.6T transceivers, VCSELs fail at 200G/lane on reliability; Nvidia uses SiPho DR rings (lowest optical insertion loss); Broadcom (Tomahawk 6 CPO) uses SiPho MZI. Author dismisses vendor arguments as philosophical: ship units at 20%+ gross margins and pass GR-468 — only Nvidia and Broadcom appear on track for 2026. DWDM ring buses face unsolved thermal crosstalk when all rings are active simultaneously. Micro-LED (referencing a Microsoft paper) is dissected as not ready: demo used only 25/100 channels (hiding crosstalk), pre-FEC BER of ~1e-7 does not meet real-world 1e-9 targets, and the new 200G Ethernet standard (IEEE 802.3dj) requires post-FEC 2e-13.

**Reliability.** Standard electronics HTOL is 1,000 hours. Optical components must pass GR-468, a hard customer requirement at 5,000 hours — 5× harder with far less EDA support.

**Electronics integration.** GlobalFoundries' "Fusion" node (45nm CMOS monolithically integrated with photonics) is universally derided across 40+ engineer interviews: inadequate node, massive crosstalk, poor yield, slow cycle time, excessive cost. TSMC COUPE (hybrid bonding of EIC + PIC) is technically excellent but too expensive for pluggable transceivers; viable for CPO only.

**Earnings commentary.** Lumentum (LITE): sold out, migrated 3-inch to 4-inch InP wafers, sold out again; ramping CW laser power from 70 mW to 100 mW toward 250–350 mW ultra-high-power class; clear CPO pipeline-cleaning for Nvidia H2 2026 ramp; hints at Broadcom CPO ELSFP engagement. Coherent (COHR): author skeptical of 6-inch InP yield claims (still buying EML from Lumentum), VCSEL-at-200G reliability position contradicts Broadcom stopping at 100G/lane, OCS insertion loss (3 dB) criticized. Keysight (KEYS): author bought more shares with Verizon proceeds.

## Calls

- [[LITE]] — LONG — n/a — Sold out on InP capacity, ramping ultra-high-power CW lasers, clear leader supplying Nvidia and Broadcom CPO ramp in 2026
- [[COHR]] — SHORT — n/a — Skeptical of 6-inch InP yield claims, VCSEL-at-200G reliability thesis contradicted by Broadcom's own 100G/lane ceiling, buying EML from competitor undermines yield narrative
- [[GFS]] — SHORT — n/a — Fusion node universally derided by engineers: 45nm electronics inadequate for CPO, massive crosstalk, poor yield, slow cycle time
- [[KEYS]] — LONG — n/a — Author added to position with Verizon proceeds; previously designated a "screaming buy"
