---
type: source
title: "High Bandwidth Flash and Sandisk Investor Day 2025"
tags: []
related: []
created: 2025-02-13
updated: 2025-02-13
authors: [irrationalanalysis]
year: 2025
url: "https://irrationalanalysis.substack.com/p/high-bandwidth-flash-and-sandisk"
venue: Irrational Analysis
post_date: 2025-02-13
tickers: [WDC, ONTO]
---

[[irrationalanalysis]] publishes a skeptical teardown of the Sandisk Investor Day 2025 and the "High Bandwidth Flash" (HBF) concept, framing it as a marketing red herring with deep fundamental flaws.

The author holds a short position in WDC (Western Digital), specifically because of the NAND flash business that is being spun out as Sandisk. The note signals that the short will likely need to be restructured post-spinout — covering WDC and re-shorting the new standalone Sandisk entity.

On Sandisk's QLC claims: the author calls the "QLC without compromise" messaging unsubstantiated, drawing a parallel to Intel's Lunar Lake AI power management claims at Hot Chips 2024 — impressive-sounding slide content with no rigorous A/B data backing it up. The competitive benchmark slide names no competing product, and Sandisk does not show its own product with hardware accelerators disabled versus enabled, which would be the honest apples-to-apples comparison.

On supply/cycle claims: Sandisk asserts its business will be more stable going forward. The author is dismissive — Samsung and Micron have cut NAND wafer starts, but YMTC has not, meaning the competitive supply overhang has not been resolved.

The core of the post is a technical demolition of "High Bandwidth Flash." Sandisk claims HBF uses the same electrical interface as existing storage with only minor protocol changes, suggesting minimal controller complexity. The author identifies this as contradictory: if the changes are truly minor, there is no need for a standards body. More critically, NAND flash has severe architectural mismatches with HBM use cases: (1) write endurance — NAND cells wear out and require over-provisioning; no architectural fix was disclosed; (2) read/write granularity — NAND pages are 4–16 KB, while HBM3 operates on 32-byte packets, a ~500x mismatch that existing software is not designed to handle; (3) silent data corruption risk — AI researchers already flag SDC as a serious problem, and NAND wear-out would make this dramatically worse. The author concludes the controller changes required are massive, not minor.

ONTO Innovation is mentioned as a data point: it just reported earnings showing NAND CapEx is rising industry-wide, meaning Sandisk's decision to deprioritize layer scaling does not eliminate competitive pressure — rivals keep running the race.

## Calls

- [[WDC]] — SHORT — px@n/a — shorting Western Digital due to the NAND/Sandisk business; will restructure to short Sandisk directly post-spinout
- [[ONTO]] — MENTION — px@n/a — cited as evidence that NAND CapEx is rising broadly, reinforcing competitive pressure on Sandisk
