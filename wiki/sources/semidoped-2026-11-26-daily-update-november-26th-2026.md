---
type: source
title: "Semi Doped — Daily Update November 26th, 2026"
tags: []
related:
  - "[[semidoped]]"
  - "[[NVDA]]"
  - "[[AMZN]]"
  - "[[285A.T]]"
  - "[[005930.KS]]"
  - "[[000660.KS]]"
  - "[[geopolitics-export-controls]]"
  - "[[custom-silicon-asic]]"
  - "[[nand-flash-storage]]"
  - "[[hbm-memory]]"
  - "[[memory-dram-cycle]]"
  - "[[ai-debt-financing]]"
created: 2026-11-28
updated: 2026-11-28
authors: [semidoped]
year: 2026
url: "https://daily.semidoped.com/p/daily-update-november-26th-2026"
venue: Semi Doped
post_date: 2026-11-26
tickers: [NVDA, AMZN, 285A.T, 005930.KS, 000660.KS]
---

Nvidia halts server shipments to four Southeast Asian countries and the region's DC lenders hit the brakes; Trainium3 posts a cost-per-token win on SemiAnalysis's benchmark; Kioxia wants SSDs to pass as GPU memory; Washington spares memory chips from new overcapacity tariffs but names Korea's subsidies.

- **Nvidia halts server shipments to Malaysia, Singapore, Thailand, Indonesia** (FT, 3 sources) — told Dell/Supermicro to stop; unclear if temporary while complying with last week's remote-access rule. Singapore booked $104B of Nvidia FY25 revenue (some is TW/CN routed through SG). Lenders paused loans tied to ByteDance/Alibaba/Tencent, led by a $6.6B upsized loan for Bain's Bridge Data Centres (Malaysia). DCs serving restricted Chinese firms have 90 days to win a license; "nobody knows how to apply." Vik: if Nvidia hardware shipments slow, that's bad news. → **NEUT [[NVDA]]** (also: S&P put Nvidia's AA on **CreditWatch Negative** over the Huang exit/return board-oversight questions). → [[geopolitics-export-controls]].
- **Trainium3 beats GB300 on cost in SemiAnalysis AgentX** — Amazon's first Trainium3 UltraServer result: **2.28× the perf-per-$ of GB300 NVL72** at one interactivity point, beats B300 and MI355X too. Almost all the edge is cost: SA models a Trainium3 chip-hour at $1.05 vs $2.31 for GB300 (per-chip throughput only ~4% higher). Modeled hyperscaler costs, preview. Nvidia's Vera Rubin NVL72 shows 3.3× Trainium3's tokens/$ on the same board; Google TPU joined InferenceX same day. → **LONG [[AMZN]]** (two biggest custom-silicon rivals now publishing tokens/$, Nvidia's own metric). → [[custom-silicon-asic]].
- **Kioxia + Nvidia turn SSDs into extra GPU memory** — GB200 NVL72 rack using Nvidia SCADA to treat 144 Kioxia SSDs (~1.1PB flash) as GPU-memory extension, reading 512-byte chunks (single vectors for vector/graph DBs). HBM is scarce; agent "lookups" can live on flash if the GPU reaches it directly. **Kioxia GP2** PCIe 6.0 SSD on XL-FLASH, >18M random reads/s at 512B, samples end-2027. Proof of concept (no speed/latency/power given). Vik: a constant search to optimize away from HBM. → **LONG [[285A.T]]**. → [[nand-flash-storage]].
- **USTR Section 301 overcapacity ruling** — 14 economies (incl. Korea/Taiwan/Japan) run distorting industrial policy; **semiconductors exempt** from the proposed Korea tariffs (covered by separate Section 232 — DRAM/NAND/HBM/equipment). But the report names Korea's K-Semiconductor Belt a distortion and USTR could raise the all-goods tariff to 25% from 15% → read as leverage to push Samsung/SK toward more US investment. → [[geopolitics-export-controls]].
- **SK hynix dates 3D DRAM** — mass production ~2031, first product 100 stacked layers (~75 to match today's 10nm-class density); existing tools build the first 100, but 200-300 layers need dedicated equipment; long term borrows NAND multi-tier stacking + hybrid bonding past 1,000 layers; studying IGZO channel. Vik: sounds like a science project. → [[memory-dram-cycle]].
- Chatter: Micron could pause NT$1.6T Taiwan investment / close Taoyuan (~3,000 jobs) if the union dispute drags; Nvidia CoWoS demand +57% to ~1.22M wafers in 2027 but its TSMC CoWoS share falls to 45.6% from 53.4% as TPU/ASICs take more; SpaceX cut small-cluster Blackwell rental to $10-12/GPU-hr; Anthropic handing back ~50k H200s. Sector: SK hynix hiring TSMC-3nm engineers for custom HBM base dies; Samsung MD310 CXL 3.2 samples early 2027; Korean 8-inch lines full on AI power chips; some FC-BGA substrate tool lead times ~30 months (from six); CoreWeave banks to sell a $4.5B GPU-backed (Meta contract) loan; UBS sees Chinese suppliers 88% of China AI-accelerator market by 2028 (Cambricon/Biren).

## Calls
- [[NVDA]] — **NEUTRAL** @ 149.30 — halts server shipments to 4 SE-Asian countries ($104B Singapore rev exposure); S&P AA on CreditWatch Negative
- [[AMZN]] — **LONG** @ 244.43 — Trainium3 2.28× perf/$ of GB300 on SemiAnalysis AgentX; Decart $7.5B buy lifts token economics
- [[285A.T]] — **LONG** @ 8450 — SSD-as-GPU-memory PoC w/ Nvidia SCADA (1.1PB flash) + GP2 PCIe6 XL-FLASH (18M IOPS); SK hynix top holder (¥)
