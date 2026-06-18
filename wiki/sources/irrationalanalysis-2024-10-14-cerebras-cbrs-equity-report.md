---
type: source
title: "Cerebras (CBRS.O) Equity Research Report"
tags: []
related: []
created: 2024-10-14
updated: 2024-10-14
authors: [irrationalanalysis]
year: 2024
url: "https://irrationalanalysis.substack.com/p/cerebras-cbrso-equity-research-report"
venue: Irrational Analysis
post_date: 2024-10-14
tickers: [CBRS, NVDA, AMD, TSM, QCOM]
---

[[irrationalanalysis]] published this 43-page engineering-driven equity research report on Cerebras Systems ($CBRS.O) ahead of its IPO, based on analysis of the draft S-1 filing (publicly released September 30, 2024). The author has followed Cerebras since 2019 and holds no economic interest in the company at time of publication.

The overall stance is broadly negative. The Wafer-Scale Engine (WSE-3) is acknowledged as a genuine engineering marvel — 900,000 cores across 84 dies on a single TSMC N5 wafer, with proprietary cross-reticle stitching invented by Cerebras — but deep structural flaws undermine the investment case.

**Key bear arguments:** (1) Massive related-party revenue concentration: G42 represented 83% of 2023 revenue and 97% of H1 2024 hardware revenue. (2) Gross margins are only 36%, far below the 60%+ expected for a hardware AI accelerator, because BOM is dominated by off-the-shelf AMD CPUs, AMD/Xilinx FPGAs, optical transceivers, and DDR5 DRAM used in SwarmX and MemoryX scale-out systems. CS-3 ASP is estimated at ~$126K with COGS ~$71K. (3) G42 holds a dilutive option to purchase shares at $14.66/share (a 17.5% discount to trailing 30-day common equity price), triggerable if a single order exceeds $500M — with G42 already committed to $1.43B by February 2025, making dilution near-certain (author assigns 99.9% probability). (4) The IPO includes an unusual early lockup release clause: if the stock trades 25% above IPO price for two of the first five trading days, insiders (including VCs) can sell up to 20% of vested holdings immediately. (5) The CSoft compiler is inadequate — riddled with hand-coded assembly, poor FLOPS utilization, no seamless PyTorch integration as marketed. (6) Inference benchmarks are misleading, using impractically small input/output token sequences (128 prompt / 20 output tokens). Running Llama 3.1 70B requires four WSE-3 systems at economics that do not scale.

**Technology limitations:** The WSE has no main memory (MemoryX is AMD CPU servers with a custom Linux kernel driver), lacks FP8 support (a significant gap vs. Nvidia Blackwell pushing FP4), has no matrix engine, and relies on expensive AMD/Xilinx FPGAs for I/O SerDes conversion. SRAM scaling has essentially stalled at 3nm-class nodes, constraining the core WSE advantage. The path to fix these issues — optical wafer bonding — is assessed as a 2029/2030 innovation at best.

**2027 scenario analysis:** Bear case (70% probability) = $5B market cap, $500M hardware revenue, 40% gross margins. Ultra Bear (25%) = <$1B market cap, revenue near zero if G42 loses interest. Bull (5%) = $50B market cap. Ultra Bull (0.01%) = $500B, full Nvidia competitor.

The author is long NVDA (30.5% net weight, avg price $16.53) and short QCOM (-18.3% net weight, avg price $163.08), with NVDA cited as the dominant beneficiary of AI training/inference infrastructure given CUDA moat built since 2007. AMD is mentioned as a fast follower on FP4 with its MI350X product (Q4 2025) but with ROCm software significantly lagging CUDA in FLOPS utilization.

## Calls

- [[CBRS]] — SHORT — px@n/a — IPO is primarily exit liquidity for insiders; G42 revenue concentration, dilutive options, low gross margins, and compiler inadequacy put company on path to irrelevance
- [[NVDA]] — LONG — px@16.53 — CUDA moat, scale-out NVLink innovation, and Blackwell FP4/FP8 roadmap leave Cerebras far behind; author's largest position
- [[AMD]] — MENTION — px@n/a — MI350X FP4 follower in Q4 2025, CDNA FLOPS utilization still well below Hopper due to ROCm software gap; AMD CPUs and Xilinx FPGAs are commodity BOM components inside Cerebras systems
- [[TSM]] — MENTION — px@131.58 — TSMC manufactures WSE-3 on N5 but charges a premium for low-volume semi-custom wafers; author holds position (6% net weight)
- [[QCOM]] — SHORT — px@163.08 — author's largest short; QCOM partnership with Cerebras for inference was abandoned in August 2024
