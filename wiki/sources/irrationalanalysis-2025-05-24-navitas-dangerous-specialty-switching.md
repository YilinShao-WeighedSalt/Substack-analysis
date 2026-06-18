---
type: source
title: "Navitas: Dangerous and Obscure Specialty Switching Regulator Company"
tags: []
related: []
created: 2025-05-24
updated: 2025-05-24
authors: [irrationalanalysis]
year: 2025
url: "https://irrationalanalysis.substack.com/p/navitas-dangerous-and-obscure-specialty"
venue: Irrational Analysis
post_date: 2025-05-24
tickers: [NVTS, MPWR]
---

[[irrationalanalysis]] opens with a blunt warning: Navitas (NVTS) is a "very dangerous stock" and 99% of readers should not touch it. The author personally lost ~$1,500 day-trading NVTS off a press release announcing a potential collaboration with Nvidia on next-generation 800V HVDC architecture for Rubin racks. Despite the loss, the author is intrigued enough to analyze whether the underlying technology is credible.

**Technical Primer — Switching Regulators**

Switching regulators convert high-voltage DC to lower-voltage DC efficiently but introduce AC noise that must be filtered. Efficiency curves are load-dependent: a 60A-rated Monolithic Power (MPWR) part actually peaks efficiency at ~15A and degrades significantly at full load. Engineers routinely over-specify systems to hit better efficiency at typical operating load.

**What Navitas Does**

Navitas manufactures GaN (Gallium Nitride) and SiC (Silicon Carbide) wide-bandgap switching regulators, claiming exclusive safety features that make them suitable for datacenter applications — including protection against inrush current and variable load stress that can destabilize or destroy expensive GPUs. The investment thesis hinges entirely on whether these claimed GaN features are real and differentiated.

**Datasheet Analysis**

The author reviews the Navitas NV6524-Q datasheet (lowest RDS_ON in their lineup — lower RDS_ON means better efficiency). Key findings:
- AEC-Q100 Grade 1 qualification: supports -40°C to +125°C operating range.
- No standard load-current-vs-efficiency plot included, but the datasheet provides enough raw parameters to calculate it independently.
- Safety features are explicitly documented with acknowledged limitations — the author views this transparency positively.
- A Navitas press release claims 97.8% efficiency for their 12kW GaN+SiC platform for hyperscale AI data centers, versus ~95% for MPWR's best parts under ideal 25°C conditions with external Vcc.

**Verdict**

The author grades Navitas datasheets A- versus MPWR's A+ for completeness, and concludes: "I think Navitas may have something." Author holds no NVTS position at time of writing; holds a very small long in MPWR.

## Calls

- [[NVTS]] — LONG (speculative/cautious) — n/a — GaN switching regulator technology may be credible for datacenter AI power delivery, but stock is extremely dangerous and illiquid
- [[MPWR]] — LONG — n/a — Small existing long; used as efficiency benchmark; rated A+ for datasheet completeness vs NVTS's A-
