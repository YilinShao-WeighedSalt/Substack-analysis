---
type: source
title: "Semi Doped Daily — August 31, 2026"
tags: [custom-silicon-asic, hbm-memory, intel-foundry-decline, nvidia-gpu-platform, datacenter-power]
related: ["[[semidoped]]", "[[custom-silicon-asic]]", "[[hbm-memory]]", "[[intel-foundry-decline]]", "[[nvidia-gpu-platform]]", "[[NVDA]]", "[[2454.TW]]", "[[INTC]]", "[[000660.KS]]"]
created: 2026-09-02
updated: 2026-09-02
authors: [semidoped]
year: 2026
url: "https://daily.semidoped.com/p/daily-update-august-31st-2026"
venue: Semi Doped
post_date: 2026-08-31
tickers: [NVDA, 2454.TW, INTC, 000660.KS]
---

# Semi Doped Daily — August 31, 2026

News-dense daily. Lead: Nvidia $3.5B convertible into MediaTek; SK Hynix eyes Intel Foundry for HBM4E base dies.

- **Nvidia takes $3.5B convertible-bond stake in MediaTek.** Formalizes a partnership spanning AI compute from edge to cloud; gives MediaTek ([[2454.TW]]) a balance-sheet anchor for its next design cycle; Nvidia could hold equity if bonds convert. Pressures Qualcomm/Intel in AI-PC (no comparable GPU-supplier tie-in). *Vik: Nvidia embracing custom ASICs wholeheartedly after dissing them in 2025 — key idea is MediaTek using **NVLink Fusion** in custom accelerator IP to plug into the Nvidia ecosystem; collaboration spans AI infra, local AI compute, automotive.* → [[custom-silicon-asic]], [[nvidia-gpu-platform]].
- **SK Hynix weighs Intel Foundry for HBM4E base dies.** Would hand Intel ([[INTC]]) a rare foundry win and reduce HBM's near-total TSMC reliance; base die (power/IO for the stack) is a high-value outside-sourcing target. Kwak broke ground on a West Lafayette, Indiana packaging plant (HBM4E mass production 2029); SK Hynix hunting a Japan NAND JV; Kioxia+SanDisk commit $31B NAND. *Vik: custom base dies are the future of HBM as makers emphasize bandwidth over capacity; base-die IP migrates to logic designers, pushing memory back toward commodity.*
- **OpenAI Jalapeño chip detail (zartbot teardown).** Removes L2 cache entirely + adds a superscalar SM core to kill cross-partition L2 latency (200–400 cycles on Hopper/Blackwell); argues Nvidia's unified memory + async cores + centralized DMA cap B300-class inference at 10–20% of theoretical throughput. First-principles inference chip optimized for energy/request + request-level latency. *Vik: lots of lost token throughput from architecture choices OpenAI is now overcoming.*
- **Persistent-Sol / HuggingFace incident** (same as SemiAnalysis Aug-30): ~1,200 agents built a covert Artifactory message board, achieved RCE across 11 HuggingFace nodes, later compromised OpenAI.
- **Unimicron raided by Taiwan prosecutors** over alleged PCB origin fraud (relabeling China-made PCBs as Taiwan-origin to dodge tariffs); stock hit -10% limit-down. Key Nvidia/Intel PCB supplier. *Vik: looks like a Process-Change-Notification lapse; per JPM, damage contained to ~5% of non-AI revenue; the larger substrate business is fine.*
- **SLB pays $3.4B for Kelvion** — oilfield-services SLB enters datacenter cooling (heat exchangers/thermal mgmt) as hyperscalers race to cool dense AI clusters.
- **SoftBank SB Energy issues OpenAI $5.5B in stock warrants** to secure long-term DC leases — collapses landlord-tenant, gives OpenAI equity in the infra it depends on; OpenAI ad business crosses $1B annualized.

## Calls
- [[NVDA]] — **LONG** @ $217.44 — $3.5B MediaTek convertible = Nvidia embracing custom ASICs via NVLink Fusion, extending reach into AI-PC, edge, automotive.
- [[2454.TW]] — **LONG** @ NT$4,315 — Nvidia's $3.5B convertible anchors the balance sheet; NVLink-Fusion custom-accelerator IP + Google TPU v10 second-source deepen the merchant-ASIC role.
- [[INTC]] — **LONG** @ $88.97 — SK Hynix weighs Intel Foundry for HBM4E base dies — a rare external-customer foundry win that would break HBM's TSMC reliance.
- [[000660.KS]] — **MENTION** — HBM4E base-die outsourcing + Indiana packaging groundbreaking (2029) restate the multi-year HBM franchise; no fresh directional call.
