---
type: source
title: "GB200 Hardware Architecture - Component Supply Chain & BOM"
tags: []
related: []
created: 2024-07-17
updated: 2024-07-17
authors: [semianalysis]
year: 2024
url: "https://newsletter.semianalysis.com/p/gb200-hardware-architecture-and-component"
venue: SemiAnalysis
post_date: 2024-07-17
tickers: [NVDA, ALAB, AVGO, MRVL, APH]
---
[[semianalysis]] delivers a comprehensive A-to-Z breakdown of Nvidia's GB200 rack architecture, covering four form factors, hyperscaler customization, and a Bill of Materials for over 50 subcomponents — revealing that deployment complexity increases dramatically versus prior HGX Hopper generations while actual NVLink copper costs are far lower than investor estimates suggested.

**Form factors and power.** Four configurations exist: NVL72 (120 kW/rack, 18 compute trays, 9 NVSwitch trays) will be rarely deployed due to datacenter power density constraints; NVL36x2 (2×66 kW racks interconnected, maintaining non-blocking all-to-all across 72 GPUs) is the dominant deployment; NVL36x2 Ariel (custom 1:1 CPU-to-GPU Bianca→Ariel swap, primarily for Meta recommendation systems); and x86 B200 NVL72/NVL36x2 (Miranda, arriving Q2 2025 with lower upfront cost but reduced CPU-GPU bandwidth and higher peak power).

**Compute tray architecture.** The Bianca board (1 Grace CPU + 2 Blackwell GPUs on one PCB) eliminates the need for PCIe retimers between CPU and GPU in the reference design — a headline negative for Astera Labs. However, custom hyperscaler designs (notably Amazon's custom backend NIC requiring a dedicated PCIe switch) still require Astera Labs or Broadcom PCIe switches, and retimers remain in other deployment contexts. ConnectX-7/8 NICs are now mezzanine-mounted directly on the Bianca board.

**NVLink interconnect cost reality.** The report corrects a widely-circulated investor estimate (attributed to Coatue) of ~$3k NVLink copper cost per GPU ($216k/NVL72 rack) as "completely wrong." Actual cost is dominated by termination and connectors, not cable runs. Amphenol's Paladin HD backplane is the primary connector source. An NVL72 uses 5,184 copper differential-pair cables. NVL36x2 requires an additional 162 1.6T ACC cables between racks plus 324 DensiLink flyover cables (>$10k in cables alone), making NVL36x2 copper content more than double NVL72 — yet still well below investor estimates. NVL576 (576 GPUs, two-tier fat-tree with optical L1→L2 connections) carries additional BOM of $5.6M/rack (~$9.7k/GPU supplier cost; ~$38.8k/GPU at 75% gross margin), making it economically untenable — the same reason DGX H100 NVL256 never shipped.

**Optics and DSP supply chain.** Transition from ConnectX-7 (400G SR4 multimode) to ConnectX-8 (800G DR4 single-mode EML, with 200G VCSEL delayed 9–18 months) reshapes the transceiver supply chain. Marvell held 100% DSP share on H100; Broadcom is now gaining significant share on GB200 through Innolight and Eoptolink. Nvidia has taped out an internal 1.6T DSP but faces power/cooling constraints limiting near-term ramp. Eoptolink joins Fabrinet and Innolight as major optical assemblers.

**Hyperscaler customization.** Google reverted to ConnectX-8 (dropped Intel IPU custom solution). Amazon uses a custom 400G backend NIC requiring adapter mezzanine boards and a dedicated PCIe switch, delaying time-to-market. Oracle is the primary Bluefield-3 frontend NIC user. xAI uses Bluefield-3 in NIC mode (not DPU mode) as a workaround for Spectrum-X Ethernet.

## Calls

- [[NVDA]] — MENTION — n/a — GB200 rack ecosystem analysis; NVL36x2 is dominant form factor, NVL576 deemed economically untenable; product complexity rises sharply generation-on-generation
- [[ALAB]] — MENTION — n/a — Retimers removed from GB200 reference design (~35% short interest at time of writing), but still required in Amazon custom NIC designs and other hyperscaler variants; market over-extrapolated the reference design impact
- [[AVGO]] — MENTION — n/a — Gaining DSP share from Marvell's prior monopoly on Nvidia transceivers; also supplying PCIe switches for custom NIC hyperscaler designs and Tomahawk backend switches
- [[MRVL]] — MENTION — n/a — Losing 100% DSP share on Nvidia optics to Broadcom as GB200 ramps; competitive pressure from both Broadcom and Nvidia's internal DSP effort
- [[APH]] — MENTION — n/a — Primary source for NVLink Paladin HD backplane connectors and SkewClear EXD Gen 2 cables; large volume beneficiary of copper-over-optical NVLink decision
