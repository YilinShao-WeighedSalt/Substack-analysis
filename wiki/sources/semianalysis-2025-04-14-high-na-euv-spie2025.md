---
type: source
title: "High-NA is Here (for R&D), EUV Cost, Pattern Shaping Gaining Share, 6x12' Mask, Metal Oxide & Dry Resist, Hyper-NA"
tags: []
related: []
created: 2025-04-14
updated: 2025-04-14
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/spie2025"
venue: SemiAnalysis
post_date: 2025-04-14
tickers: [ASML, INTC, AMAT, 8035.T, LRCX]
---

[[semianalysis]] covers SPIE Advanced Lithography & Patterning 2025, detailing progress on High-NA EUV lithography tools, mask infrastructure, photoresist transitions, and complementary patterning techniques that will define semiconductor manufacturing at the 14A node and beyond.

**High-NA Manufacturing Readiness (Intel).** Intel's Steve Carson delivered the keynote on their two fully installed ASML EXE:5000 High-NA EUV tools, having run 30,000 wafers across both systems. Key firsts: factory integration and testing were skipped — the first fully built EXE:5000 was tested directly at Intel, an unprecedented step for a new scanner generation. Source power reached 110% of target (vs. 15% for the first NXE:3300 and 50% for the NXE:3400B at equivalent milestones), and reliability was at 85% — both well ahead of prior new-tool ramps. Overlay to low-NA tools came in at 0.6nm, sufficient to declare no penalty for stitched-field exposures needed on large dies. Intel declared both tools "in production" (running wafers on a proven process, not commercial products), likely on 18A.

**High-NA Cost Analysis (IBM).** IBM's Luciana Meli presented the only cost-focused talk. Key finding: a single High-NA exposure costs ~2.5x a single low-NA exposure. High-NA only beats low-NA on cost when it replaces three or more low-NA masks — IBM estimates a four-mask low-NA SALELE process is 1.7–2.1x more expensive than a single High-NA pass. For double-patterning, low-NA remains cheaper. This tightly limits the economically justified High-NA insertion points at 14A to specific metal and contact-hole layers using triple or quadruple EUV. IBM also flags that High-NA single-exposure metal may miss tip-to-tip design targets, requiring directional etch tools (e.g., AMAT Sculpta) as a fix.

**6×12" Mask Infrastructure.** Intel called to action the industry on adopting a 6×12" mask (doubling the industry-standard 6×6" size in use since the 1980s), which would improve scanner throughput 23–50% and eliminate field-stitching issues. ASML acknowledged progress but said large-mask capability may arrive "early in the next decade" — after 14A. Obstacles include redesigning the entire mask ecosystem (blanks, e-beam writers, cleaning, fab handling) — analogous in scope to the 200mm-to-300mm wafer transition. ASML's financial incentive also favors selling two standard-mask High-NA tools over one large-mask tool.

**Metal Oxide Resist (MOR) & Wet vs. Dry.** MOR resists offer better resolution, line-edge roughness, and etch selectivity than conventional chemically amplified resists (CAR), critical for the very thin films required by High-NA's reduced depth of focus. The economic crossover point for MOR/High-NA insertion is estimated at ~30nm pitch vias, expected at the A10 node (~2 nodes out). TEL (Tokyo Electron) is the incumbent with wet spin-coat and wet develop; Lam Research is challenging with dry resist deposition and dry etch-to-develop. Winners in this wet-vs.-dry battle are beginning to emerge in research results covered in the paywalled section.

**Pattern Shaping & Complementary Techniques.** AMAT's Sculpta directional etch tool and TEL's Acrevia are gaining share as complementary techniques to EUV, enabling patterning outcomes (e.g., metal tip-to-tip control) that High-NA single exposure alone cannot achieve. Directed self-assembly (DSA) is also gaining attention. ASML is already developing Hyper-NA concepts for the CFET era beyond 14A, targeting a common platform across NXE, EXE, and future tools.

## Calls

- [[ASML]] — LONG — n/a — dominant monopoly on EUV and High-NA scanners; EXE:5000 at ~$400M is performing above spec on source power and reliability, with clear roadmap to Hyper-NA; only risk is large-mask investment delaying unit economics improvement
- [[INTC]] — MENTION — n/a — first mover on High-NA EUV with two installed tools and 30,000-wafer head start; 14A node strategy depends on High-NA for select metal layers but feasible without it
- [[AMAT]] — LONG — n/a — Sculpta directional etch tool gaining share as necessary complement to High-NA EUV single-exposure, addressing tip-to-tip metal patterning shortfall; IBM explicitly calls it out as required
- [[8035.T]] — MENTION — n/a — TEL's Acrevia pattern-shaping tool and wet-track resist processing (spin-coat + wet develop) are incumbents under challenge from Lam's dry resist approach
- [[LRCX]] — MENTION — n/a — dry resist deposition and etch-to-develop platform competing with TEL's wet track for MOR market share at critical High-NA layers; outcome still being decided in research
