---
type: source
title: "A Background-Proof Guide on Process Development Kits"
tags: []
related: []
created: 2025-01-24
updated: 2025-01-24
authors: [irrationalanalysis]
year: 2025
url: "https://irrationalanalysis.substack.com/p/a-background-proof-guide-on-process"
venue: Irrational Analysis
post_date: 2025-01-24
tickers: [TSM, INTC]
---

[[irrationalanalysis]] publishes a comprehensive educational deep-dive into Process Development Kits (PDKs) — the most NDA-protected, least publicly understood component of semiconductor development. The post is framed as accessible to all readers and draws on four textbooks alongside the author's industry experience since 2011.

A PDK contains three primary categories: standard cell libraries (transistors, RLC components, higher-level blocks), models for process/voltage/temperature (PVT) sensitivity, and extensive documentation on cell placement, yield improvement, and parasitic mitigation. The post walks through ideal device theory (resistors, capacitors, inductors, MOSFETs), process stackups, and design rules before diving into the practical failure modes designers must simulate against.

Key practical issues covered include device parasitics (even simple capacitors behave like inductors at high frequencies), wire network parasitics, electromagnetic coupling, process variation (SS/FF/TT/FS/SF corners), temperature sensitivity, voltage uniformity (power grid distribution across tens of billions of transistors), electromigration, and leakage/noise. The author explicitly ties Intel's Raptor Lake (13th/14th gen) degradation failures to electromigration from skipping standard HTOL testing — a test that costs under $100K — calling Intel's excuses about microcode and "unintended excessive voltage" disingenuous.

On Design-Technology Co-Optimization (DTCO), the post explains how Nvidia's "4N" node designation reflects custom TSMC modifications (alternative metal stackups, relaxed design rules, shifted process corners). Derivative nodes (e.g., TSMC N6, N4, N3P; Intel 3 from Intel 4, Intel 18A from Intel 20A) offer asymmetric R&D returns but are not step-function improvements.

The foundry landscape section is pointed: Samsung Foundry is dismissed as hopeless on yield. Intel's 18A situation is analyzed in detail — the author argues that Intel VP "Mr. Sell" publicly claiming D0 < 0.4 on 18A (a statement subject to securities liability) is technically true but misleading, because defect density and parametric yield are separate metrics. The cancellation of the parent node Intel 20A is treated as strong evidence the entire node family is structurally broken, making 10% overall yield on Panther Lake (the rumored figure from Reuters) entirely plausible. On TSMC, the author holds a large long position and expects to maintain it for approximately two years, viewing the low P/E as a geopolitical risk discount (involuntary merger with SMIC) rather than a fundamental flaw.

## Calls

- [[TSM]] — LONG — n/a — author holds large TSMC position, expects to own for ~2 years; low P/E reflects geopolitical tail risk, not business quality
- [[INTC]] — SHORT — n/a — Intel 18A/20A node family structurally broken; PDK quality issues, skipped HTOL testing on Raptor Lake, 10% Panther Lake yield rumor credible
