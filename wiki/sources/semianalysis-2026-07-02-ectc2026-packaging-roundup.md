---
type: source
title: "ECTC 2026 Roundup: EMIB-T, Custom HBM, Microfluidic Cooling, Photonics"
tags: [advanced-packaging, hbm-memory, co-packaged-optics, intel-foundry, cooling]
related: ["[[semianalysis]]", "[[INTC]]", "[[TSM]]", "[[MRVL]]", "[[005930.KS]]", "[[000660.KS]]", "[[MU]]", "[[NVDA]]", "[[AMD]]", "[[advanced-packaging]]", "[[hbm-memory]]", "[[co-packaged-optics]]"]
created: 2026-07-04
updated: 2026-07-04
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/ectc2026"
venue: SemiAnalysis
post_date: 2026-07-02
tickers: [INTC, TSM, MRVL, 005930.KS, 000660.KS, MU, NVDA, AMD, AMKR]
---

# ECTC 2026 Roundup

Technical roundup of the premier advanced-packaging conference. Thesis: transistor scaling has slowed, so **packaging is now the primary scaling vector** — but packages themselves are hitting size, I/O, and thermal limits.

**Intel EMIB-T** — next-gen embedded silicon bridge with TSVs for direct power delivery (cuts DC voltage drop 68–80%). Validated at 36/35 µm bump pitch on 2× reticle silicon; scaling to 4.5× reticle by end-2026, testing 25 µm pitch. Quarter-panel (240×240mm, ~67 reticles) shown but with severe warpage. 10 metal layers, MIM caps (500 nF/mm²). Enables HBM4E at 12+ Gb/s. SA: **"most credible alternative to TSMC CoWoS"**, expected in **Google TPU v9** — but "still catching up to an ecosystem executing in volume for years" (TSMC ahead on DTC, integrated voltage regulators, active LSI).

**Marvell Custom HBM** — replaces JEDEC-standard HBM base die with custom logic base die on advanced node; cuts host-ASIC HBM PHY footprint ~60%, shortens interposer channel 6.5→1.5mm, uses cheaper organic RDL interposer. Nvidia Feynman + AMD MI450 (LPDDR expansion) heading same way. ~16% of Rubin GPU die is HBM logic that custom HBM offloads.

**Samsung** — 8-layer Si interposer for HBM4E (20% fewer layers); HBM hybrid-copper-bonding (HCB) thermals: stack-level resistance −19% to −29% vs TCB. Also **VCS** (Vertical Cu post Stack) for mobile DRAM: −41% power, no TSVs.

**Microfluidic cooling** — TSMC micropillar direct-to-silicon on CoWoS-R (5.3 kW at 8 LPM); **Microsoft** straight microchannels on real Nvidia GH200 (−50% package thermal resistance, 6-mo reliability data). TSMC only 3 papers vs Intel's 12, Samsung's 11.

**Optics** — Marvell OMIB + Photonic Fabric (from Celestial AI acquisition): embedded PIC in organic RDL interposer, 1.8 Tbps/mm²; uses electro-absorption modulators (EAMs) not ring modulators — SA: EAMs "difficult to manufacture at scale." **Lightmatter Passage M1000** multi-reticle photonic interposer, 15 chiplets, >95% assembly yield despite ~59µm warpage.

**Other:** hybrid bonding to 450nm pitch (AMAT/EVG); glass-core substrates (Intel 510×515mm 24-layer, Amkor/STATS ChipPAC); interposer alternatives (IBM DBrM, Unimicron); RDL scaling toward 1/1 µm L/S driven by UCIe 3.0.

## Calls
- [[INTC]] — NEUTRAL/constructive — EMIB-T credible CoWoS alternative, Google TPU v9-bound, but "still catching up to TSMC." px@call 120.35
- [[MRVL]] — LONG — custom HBM + OMIB/Photonic Fabric (Celestial) validate optics/packaging roadmap; EAM scale risk flagged. px@call 245.29
- [[TSM]] — LONG — CoWoS remains dominant, leads microfluidic cooling; challengers only now appearing. px@call 446.68
- [[005930.KS]] — NEUTRAL — HBM4E interposer + HCB thermals + VCS mobile DRAM progress. px@call 309500 (KRW)
- [[NVDA]] — MENTION — Feynman adopts custom HBM; Rubin GPU ~16% die is HBM logic. px@call 194.44
- [[MU]] — MENTION — custom HBM theme; memory-layer value migration. px@call 975.56
