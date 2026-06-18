---
type: source
title: "Clash of the Foundries: Gate All Around + Backside Power at 2nm"
tags: []
related: []
created: 2024-10-01
updated: 2024-10-01
authors: [semianalysis]
year: 2024
url: "https://newsletter.semianalysis.com/p/clash-of-the-foundries"
venue: SemiAnalysis
post_date: 2024-10-01
tickers: [TSM, INTC, AMAT, ASML]
---

[[semianalysis]] argues the semiconductor industry is at a critical inflection point as FinFET scaling has exhausted and two new paradigms — gate all around (GAA) transistors and backside power delivery networks (BSPDN) — must be adopted across all leading-edge foundries within 2–3 years.

**TSMC** won the FinFET era decisively; nearly all leading-edge logic is manufactured on its N5/N3 nodes. With N2 entering high-volume production in 2025, TSMC is first among the major foundries to deploy GAA without BSPDN, followed by N2P/N2X variants and A16 (GAA + backside contacts) in H2 2026. TSMC's conservative first-generation backside contact implementation targets ~7–10% density improvement (roughly half the theoretical maximum) to preserve N2 design compatibility, while enabling up to 20% power improvement via reduced IR drop.

**Intel** is first-to-market on a combined GAA + BSPDN node with 18A (using its PowerVia scheme). Defect density is reportedly on track, making process technology a rare bright spot amid broader financial difficulties. PowerVia is easier to fabricate than direct backside contacts but offers slightly less scaling benefit. The preceding 20A node was abandoned for financial rather than technical reasons.

**Samsung** claims to have been first in GAA production (SF3E, 2022) but in minimal commercial volume. SF2 is evolutionary; the major roadmap milestone is SF2Z in 2027, which introduces direct backside contacts delivering an 8% performance increase, 15% power reduction, and 7% area reduction. Samsung remains "customer challenged" with poor yields since 7nm.

**Rapidus**, the Japanese government-backed 2nm startup (incorporating IBM process IP), targets a pilot line in April 2025 and HVM in 2027. The post is deeply skeptical: no meaningful customer volumes (only Tenstorrent confirmed), small batch sizes increase metrology burden, no BSPDN on roadmap (a HPC disadvantage), and no clear competitive moat against TSMC, Intel, or Samsung. Rapidus is not publicly traded.

**SRAM scaling** is identified as effectively dead since 5nm — TSMC's N3 and N2 offer little bitcell scaling — with GAA providing only a one-time improvement from the FinFET-to-GAA transition.

**Backside power delivery** is covered in deep technical detail across three approaches: Buried Power Rail (simplest, likely not adopted in HVM due to metal-in-FEOL contamination risk), PowerVia (Intel's approach — avoids contamination, good scaling), and Direct Backside Contacts (highest risk/reward, best density, used by TSMC A16 and Samsung SF2Z).

**WFE implications** and 2nm fab cost modeling (paywalled section) are flagged as key downstream topics — relevant to equipment vendors including **Applied Materials** (AMAT, cited for early warnings on cobalt metallization) and **ASML** (noted for advances in post-bonding overlay capabilities enabling BSPDN).

## Calls

- [[TSM]] — LONG — n/a — TSMC extending dominance into GAA era with steady N2/A16 ramp and share price continuing to compound
- [[INTC]] — NEUTRAL — n/a — 18A process tech is on track but financial distress and lack of major external customers create significant uncertainty
- [[AMAT]] — MENTION — n/a — Key equipment supplier cited for BSPDN tooling and FEOL metallization history; WFE spend implications discussed
- [[ASML]] — MENTION — n/a — Named for post-bonding overlay advances critical to enabling backside power delivery at scale
