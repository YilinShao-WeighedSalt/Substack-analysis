---
type: source
title: "Power Semis Part 2: SiC vs GaN, Wolfspeed 10KV"
tags: []
related: []
created: 2026-04-25
updated: 2026-04-25
authors: [irrationalanalysis]
year: 2026
url: "https://irrationalanalysis.substack.com/p/power-semis-part-2-sic-vs-gan-wolfspeed"
venue: Irrational Analysis
post_date: 2026-04-25
tickers: [WOLF, NVTS, ON, POWI]
---

[[irrationalanalysis]] wrote this post as an engineering-driven explainer comparing Silicon Carbide (SiC) and Gallium Nitride (GaN) power semiconductors, prompted by reader questions about Wolfspeed's 10KV SiC announcement and the SiC vs. GaN competitive dynamic.

The author uses a worked example — a 400V-to-48V buck converter designed around Infineon 650V-class GaN and SiC parts in identical TOLL packages at similar Rds_on — to walk through the physics trade-offs. The key insight is that switching frequency governs passive component sizing: higher switching frequency shrinks the required inductor and capacitor footprint, and GaN can switch at 1 MHz or faster versus 0.1–1 MHz for SiC. At comparable switching speeds, GaN shows a dramatic parasitic advantage: the SiC part has 17.4× the gate-charge loss of the equivalent GaN part. GaN is therefore more efficient and more compact at the same switching speed.

However, GaN has a hard ceiling: commercially available GaN parts top out around 650V / 450W, with most in the 100–200W range. SiC retains dominance at higher voltages and power densities. The author frames this as GaN "encroaching on SiC territory from below" rather than displacing it.

ON Semiconductor's claims of vertical GaN capable of ~1200V are flagged with skepticism ("what was ON smoking"). A passing claim of 1700V for lateral GaN is similarly dismissed.

The most interesting data point in the post is Wolfspeed's announcement of 10KV SiC parts — described as a "unique breakthrough" with a semi-public preliminary datasheet. The author finds this genuinely interesting despite an otherwise dismissive baseline view of Wolfspeed ("recently un-bankrupt shitco," crowded SiC market). The preliminary datasheet is missing key charts (temperature and switching-speed curves), so a proper competitive comparison to Infineon's 2KV SiC parts cannot yet be made.

Navitas (NVTS) is noted as a dual SiC/GaN vendor with structural incentive to favor GaN; the author says both Navitas and Wolfspeed are "both right" from their respective vantage points. Power Integrations (POWI) is dismissed due to unreadable datasheets.

The overarching conclusion: GaN and SiC are both valid — the right choice depends heavily on voltage, power level, and footprint constraints — and only high-density (≥400W-class) GaN parts can truly compete with SiC on footprint.

## Calls

- [[WOLF]] — SHORT — px@call: n/a — dismissed as a crowded-SiC "recently un-bankrupt shitco," though the 10KV breakthrough is noted as genuinely interesting and warrants further investigation once the full datasheet is available
- [[NVTS]] — MENTION — px@call: n/a — dual SiC/GaN vendor with structural incentive to push GaN; cited as context for industry bias dynamics, no directional call
- [[ON]] — MENTION — px@call: n/a — vertical GaN 1200V claims met with skepticism; no directional call
- [[POWI]] — MENTION — px@call: n/a — skipped from analysis entirely due to poor datasheet quality; no view expressed
