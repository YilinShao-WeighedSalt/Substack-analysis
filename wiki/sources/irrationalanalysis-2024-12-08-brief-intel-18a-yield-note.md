---
type: source
title: "Brief Intel 18A Yield Note"
tags: []
related: []
created: 2024-12-08
updated: 2024-12-08
authors: [irrationalanalysis]
year: 2024
url: "https://irrationalanalysis.substack.com/p/brief-intel-18a-yield-note"
venue: Irrational Analysis
post_date: 2024-12-08
tickers: [INTC, AVGO]
---

[[irrationalanalysis]] dissects the viral 10% yield rumor surrounding Intel's 18A process node, arguing that almost every public commentator — from Korean press to Intel fan-accounts to TSMC meme pages — is either missing the point or being deliberately misleading.

The post opens by dismissing the source of the rumor: Korean semiconductor press with a strong Samsung Foundry bias. It also notes that the Broadcom test chips at the center of the story were built on PDK v0.7, an early development kit, making any yield conclusions from those chips practically meaningless. The author's main analytical move is distinguishing **functional yield** (does the chip turn on and pass basic tests?) from **parametric yield** (does it hit target clock frequency, power at load, and power at idle?). Using a detailed car-factory analogy, the post shows how a fab can claim high functional yield while parametric yield — the number that determines whether a chip is actually saleable — can be dramatically lower. Intel's publicly cited 0.4 defects-per-cm² (D0) figure addresses only the functional yield component; it says nothing about whether Panther Lake CPU core chiplets meet their performance and power targets.

The actual rumor is that Intel's Panther Lake CPU core chiplet (the largest die in the package) has an **overall yield of ~10%**, once parametric constraints are applied. The author walks through the math showing this is entirely plausible even given Intel's stated D0 figure, if PDK modeling was significantly off. Intel's decision to publish the 0.4 D0 number on the exact day the Reuters negative story broke is called out as an investor-relations move calibrated to an audience that does not understand parametric yield.

Three possible outcomes for Intel are laid out: (1) re-spin Panther Lake at a cost of 4-6 months delay; (2) ship at current yields, destroying gross margins; or (3) lower performance and power targets, releasing a product crushed by AMD, Qualcomm, and MediaTek/Nvidia competitors in the laptop market. The post closes by framing the public debate as a "Moronic Rorschach Test" — Samsung sympathizers see Intel failing; Intel bulls cite D0 as a talisman; neither side is engaging with the real issue of parametric yield. Resolution is expected when actual Panther Lake silicon performance data becomes available.

## Calls

- [[INTC]] — SHORT — n/a — 18A parametric yield likely far worse than functional yield implies; Panther Lake faces re-spin delay or margin destruction; PDK accuracy in question
- [[AVGO]] — MENTION — n/a — Broadcom test chips on early 18A PDK v0.7 are the proximate cause of the yield rumor cycle
