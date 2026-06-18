---
type: source
title: "[1/3] Dell XPS (TributoQC) 13 Review"
tags: []
related: []
created: 2024-07-27
updated: 2024-07-27
authors: [irrationalanalysis]
year: 2024
url: "https://irrationalanalysis.substack.com/p/13-dell-xps-tributoqc-13-review"
venue: Irrational Analysis
post_date: 2024-07-27
tickers: [QCOM, AAPL, MSFT]
---

Part one of a three-part series reviewing the Dell XPS 13 (internally codenamed TributoQC) powered by Qualcomm's Snapdragon X Elite. The author — a semiconductor investor writing at [[irrationalanalysis]] — approaches the review from both a consumer and a financial/technical analyst lens.

**General impressions** are largely positive on hardware: the OLED display, chassis rigidity, USB-C power delivery, and 16 GB of RAM all represent meaningful upgrades over the author's prior 2018 LG Gram. Aesthetic gripes are minor (touch bar replacing physical ESC/DEL keys; unconventional under-chassis touchpad).

**Battery life** is the central negative finding. Despite fans almost never spinning and the chassis staying cool, real-world usage comes in at only 6–8 hours under light workloads (browser, Discord, Python, light photo editing). The author attributes this to the excessive power management IC (PMIC) complexity on the motherboard: at least 56 switching regulators, 18 LDOs, and 7 PMIC chips for what is effectively 18 supply rails. The hypothesis is that Qualcomm ham-fisted an inefficient VRM solution onto OEMs, then compensated them with a ~$60/chip "marketing subsidy." If that subsidy is added back into COGS, gross margin on the X Elite collapses from ~52% to ~14%, making the much-hyped diversification chip dilutive to QCOM operating profit rather than accretive. The author references Stacy Rasgon (Bernstein) as having naively assumed 50% gross margin, and plans to use an oscilloscope and multimeter to reverse-engineer the PMIC efficiency characteristics in a future installment.

**AI PC / on-device AI** is described as a hoax. The Copilot key maps to a lazy Edge browser wrapper connecting to Bing Chat — it never invokes the on-device NPU. The only functioning NPU use-case found was live video translation, which worked but produced poor output quality. The author views this as a massive opportunity for AAPL's Apple Intelligence to demonstrate genuine on-device AI, in contrast to the "half-baked, mediocre" execution from MSFT and QCOM.

**GPU/gaming performance** is poor: Unity-engine titles run at 22–46 FPS on blank levels, and a 2018 title (Frostpunk) achieves only 7 FPS. The author attributes underperformance to immature driver quality rather than raw hardware limitations.

**Software compatibility** via Microsoft's x86-64→AArch64 emulator is praised as meaningfully improved; all tested apps installed and ran, though Electron apps (notably Discord) suffer noticeable UI lag.

## Calls

- [[QCOM]] — SHORT — n/a — $60/chip OEM subsidy wipes out X Elite gross margin, making the flagship AI PC chip dilutive to operating profit; PMIC design is inefficient and Qualcomm's AI PC execution is a marketing failure
- [[AAPL]] — LONG — n/a — positioned as the clear winner of on-device AI given Microsoft and Qualcomm's failed Copilot+ rollout
- [[MSFT]] — MENTION — n/a — Copilot+ criticized as a half-baked Edge wrapper that never uses the local NPU
