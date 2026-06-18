---
type: source
title: "Primer: Switching Regulators and VRMs"
tags: []
related: []
created: 2024-11-15
updated: 2024-11-15
authors: [irrationalanalysis]
year: 2024
url: "https://irrationalanalysis.substack.com/p/primer-switching-regulators-and-vrms"
venue: Irrational Analysis
post_date: 2024-11-15
tickers: [MPWR, NVDA]
---

[[irrationalanalysis]] uses Monolithic Power Systems' (MPWR) steep ~40% stock decline — driven by SemiAnalysis and Edgewater negative supply-chain notes about lost Nvidia allocation — as a springboard to explain the engineering fundamentals of switching regulators and voltage regulation modules (VRMs).

A switching regulator uses pulse-width modulation to step down DC voltage (e.g. 12V to 1.2V), essentially two high-power transistors whose output oscillates between V_IN and ground. Because the raw output cannot be fed directly into chips, an LC low-pass filter smooths out the ripple. Multi-phase designs — multiple regulators offset in time with combined filtered outputs — further reduce ripple and improve efficiency. The author walks through a public MPWR 100A power stage datasheet, noting that peak efficiency occurs around 40A load, well below the rated maximum; running a stage near its ceiling degrades efficiency significantly.

The central thesis is that **MPWR has no moat**. Three engineers can design out a power stage vendor in roughly one month (signal integrity, power integrity, layout). If a competitor like Infineon offers peak efficiency at a slightly lower load current, a board designer simply adds more phases, resizes the power plane, and runs the competing part at the sweet spot. The cost and complexity of such a redesign is low enough that switching vendors is a credible threat whenever pricing negotiations break down. The author briefly held MPWR shares but liquidated at a 0.5% loss after concluding the competitive position does not justify a premium valuation.

The post closes with pointed commentary on market participants who bid MPWR to a forward P/E above NVDA's without understanding the underlying product, and who panic-sold on supply-chain rumors — reinforcing the author's view that the valuation was never justified on engineering fundamentals.

Key data points: MPWR RSI touched 19 during the selloff; three-engineer, one-month design-out timeline; efficiency peak at ~40A on the 100A-rated stage; major competitors are Infineon and Renesas (with TI and Analog Devices in lower-power niches).

## Calls

- [[MPWR]] — SHORT/AVOID — n/a — No competitive moat; design-out cost is trivially low, making premium valuation unsustainable
- [[NVDA]] — MENTION — n/a — Referenced only as valuation benchmark (MPWR was bid above NVDA's forward P/E)
