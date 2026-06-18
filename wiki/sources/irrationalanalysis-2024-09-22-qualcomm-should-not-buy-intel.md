---
type: source
title: "Qualcomm should not buy any subset of Intel."
tags: []
related: []
created: 2024-09-22
updated: 2024-09-22
authors: [irrationalanalysis]
year: 2024
url: "https://irrationalanalysis.substack.com/p/qualcomm-should-not-buy-any-subset"
venue: Irrational Analysis
post_date: 2024-09-22
tickers: [QCOM, INTC, ARM, MRVL]
---

[[irrationalanalysis]] argues forcefully that Qualcomm acquiring any part of Intel would be a value-destroying disaster, triggered by a WSJ report of takeover interest that sent stocks in opposite directions shortly before market close on a Friday.

**Deal mechanics**: The author first dispenses with the idea of buying only Intel's consumer PC division (CCG) while offloading the datacenter/server unit (DCAI). IP — CPU microarchitectures, GPU cores, OneAPI software, interconnects — is deeply shared across both segments. Any acquirer must buy all of Intel Design (fabs excluded); a partial carve-out is engineering fiction.

**Redundancy catalog**: The post walks through eight product areas where a combined QCOM+INTC entity would have zero synergy or outright conflict:
- **GPU**: Qualcomm Adreno (mobile-optimized) vs. Intel Arc (discrete/integrated PC) — completely different architectures, different driver stacks. Buying Arc does nothing to fix Adreno's notoriously bad Windows GPU drivers; the author suggests simply hiring Intel GPU driver engineers directly for ~$300M in RSU grants.
- **DSP/NPU**: Qualcomm Hexagon vs. Intel Movidius — both VLIW, but incompatible compiler stacks and hand-tuned assembly libraries that cannot merge.
- **AI Software**: Qualcomm AI Stack (Hexagon-centric) vs. Intel OneAPI (multi-target) — merging teams would produce political warfare, not unified tooling.
- **CPU microarchitecture**: Qualcomm's $1.4B Nuvia acquisition delivered a competitive ARM core; Intel has multiple P-core and E-core teams. Combined entity would be grotesquely overstaffed; ARM ISA and x86 roadmaps must be maintained in parallel with almost no shared sub-blocks.
- **PC competitive positioning**: Intel's Lunar Lake gains came from migrating to TSMC N3B (3nm-class), a more expensive node that Qualcomm/AMD deliberately avoided to protect margins. Qualcomm's path is organic: improve x86-64 emulation, fix Adreno Windows drivers, design a proper laptop PMIC — not an acquisition.
- **Physical design**: Qualcomm's team already juggles TSMC and Samsung foundry ports under extreme time pressure; adding Intel foundry obligations would be unmanageable.
- **WiFi/Bluetooth**: Qualcomm's Atheros-derived stack is industry-leading; Intel's entire WiFi/BT team would be 100% redundant — headcount to be fired.
- **O-RAN**: Intel (Altera FPGAs + Xeon D) is already losing this market to custom ASICs from Qualcomm and Marvell; acquiring a declining position makes no sense.

**Motive assessment**: The author assigns 1% probability to Qualcomm management genuinely being this foolish, and 99% to CEO Cristiano Amon publicly trolling Intel — consistent with his prior history of leaking investment interest in ARM to the FT while simultaneously fighting ARM in court over the Nuvia license assignment.

**Author bias disclosed**: The author holds a large short position in QCOM and acknowledges hoping the deal proceeds so it tanks QCOM stock, allowing him to cover profitably.

## Calls

- [[QCOM]] — SHORT — px@n/a — author holds a large short; views acquisition as value-destroying and expects stock to tank if pursued
- [[INTC]] — MENTION — px@n/a — subject of the proposed acquisition; analyzed as deeply entangled (CCG/DCAI IP cannot be separated) and strategically redundant with Qualcomm's portfolio
- [[ARM]] — MENTION — px@n/a — cited as precedent for Amon's trolling behavior (floated consortium ARM investment to FT while fighting ARM in court over Nuvia)
- [[MRVL]] — MENTION — px@n/a — named alongside Qualcomm as winning O-RAN share from Intel with custom ASICs
