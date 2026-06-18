---
type: source
title: "GTC 2025: Co-Packaged Optics Switching"
tags: []
related: []
created: 2025-03-19
updated: 2025-03-19
authors: [irrationalanalysis]
year: 2025
url: "https://irrationalanalysis.substack.com/p/gtc-2025-co-packaged-optics-switching"
venue: Irrational Analysis
post_date: 2025-03-19
tickers: [ANET]
---
Written hastily from GTC 2025 in San Jose, this post reacts to Jensen Huang's public roasting of optical transceivers and digs into TSMC's COUPE (Co-packaged optics using photonic engines) technology as the architecture that makes co-packaged optics (CPO) viable at scale.

The author explains the layered architecture of photonic integration. A photonic IC (PIC) contains the optical elements — resonators, modulators, photodiodes, waveguides — but must be fabricated on a special photonic process node and is highly sensitive to electrical signal quality and temperature. A separate electrical IC (EIC), built on a standard logic node, reshapes and amplifies the signal to drive the PIC correctly. The reason the switch ASIC cannot directly drive the PIC is twofold: signal degradation over distance, and the extreme thermal sensitivity of micro-ring modulators on the PIC, which are literally temperature-controlled and cannot tolerate the heat of a co-located switch die.

TSMC's COUPE solves the EIC-PIC integration problem by hybrid bonding the two dies together rather than using conventional RDL packaging. The key benefits are substantial: 85% reduction in parasitic capacitance (which the author calls the main enemy of SerDes and package designers), near-zero insertion loss, and — most importantly — 20 dB improvement in return/reflection loss. Using a singer-in-a-reverberant-room analogy, the author stresses that return loss (echoes) is the hard problem; insertion loss (volume) is manageable. COUPE also improves power supply noise rejection (PSRR), adding system margin. The author cautions against taking the 40% energy efficiency claim at face value due to an unrealistic baseline in the TSMC paper.

Laser sources in this architecture remain pluggable because they are the primary point of failure and must be serviceable. COUPE is presented as the enabling step that makes CPO commercially credible — without hybrid bonding EIC to PIC, CPO cannot achieve the signal integrity needed for production switch deployments.

The author is bearish on transceiver-exposed companies and explicitly calls out [[irrationalanalysis]]'s view that Arista is in a precarious position as CPO threatens to commoditize or eliminate the pluggable transceiver supply chain on which its ecosystem depends. The author notes ongoing CPO research and a forthcoming detailed primer.

## Calls

- [[ANET]] — SHORT — n/a — CPO removes the pluggable transceiver ecosystem that underpins Arista's networking stack; "Arista in deep shit"
