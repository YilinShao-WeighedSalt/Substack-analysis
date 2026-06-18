---
type: source
title: "Huawei AI CloudMatrix 384 China's Answer to Nvidia GB200 NVL72"
tags: []
related: []
created: 2025-04-16
updated: 2025-04-16
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/huawei-ai-cloudmatrix-384-chinas-answer-to-nvidia-gb200-nvl72"
venue: SemiAnalysis
post_date: 2025-04-16
tickers: [NVDA, TSM]
---
[[semianalysis]] delivers a deep technical teardown of Huawei's CloudMatrix 384, positioning it as China's first credible system-level answer to Nvidia's GB200 NVL72 — and arguing that systems engineering, not raw chip performance, will define the next phase of the AI infrastructure race.

**System architecture.** CloudMatrix 384 packs 384 Ascend 910C chips into an all-to-all optical topology spread across 16 racks (12 compute, 4 switch). It delivers 300 PFLOPs of dense BF16 compute, 3.6x the aggregate HBM capacity of the GB200 NVL72, and 2.1x the memory bandwidth. The entire scale-up fabric runs on 6,912 400G LPO optical transceivers — "100% Optics, 0% Copper" — a design choice Nvidia abandoned when it shelved its own optically interconnected DGX H100 NVL256 "Ranger" program. Huawei's willingness to absorb optical complexity reflects both China's domestic strength in optical networking production and its access to abundant, cheap power.

**Power penalty.** The system is significantly less efficient than its Nvidia rival: 4.1x the absolute power draw, 2.5x worse power per FLOP, and 1.9x worse power per TB/s of memory bandwidth. The authors acknowledge this as a real disadvantage but argue it is partially offset by China's low power costs and by the system's massive memory advantages for memory-bound inference workloads.

**Supply chain and sanctions circumvention.** TSMC supplied roughly 2.9 million dies across 2024–2025, enabling approximately 1.05 million Ascend 910C packages. Huawei routed roughly $500 million in 7nm wafer orders through Sophgo to evade export controls; TSMC now faces a potential fine exceeding $1 billion for the violation. On memory, China stockpiled an estimated 13 million HBM stacks — enough for 1.6 million Ascend 910C packages — primarily sourced from Samsung before restrictions tightened. SMIC is expanding domestic advanced-node capacity toward ~50,000 wafers per month across Shanghai, Shenzhen, and Beijing fabs, backed by tens of billions in government equipment funding alongside CXMT on the memory side.

**Strategic thesis.** The core argument is that "systems matter more than microarchitecture." Huawei has demonstrated the ability to ship a coherent, large-scale AI training cluster using domestically manufactured or stockpiled components, optical interconnects, and aggressive system integration. The gap to Nvidia on per-chip efficiency is real but does not preclude CloudMatrix 384 from training frontier-scale Chinese models. The authors frame this as a structural shift: China is no longer purely dependent on Nvidia for frontier AI compute.

## Calls

- [[NVDA]] — SHORT — n/a — CloudMatrix 384 demonstrates China no longer needs Nvidia for frontier AI compute, eroding the addressable market in the world's second-largest AI infrastructure spender
- [[TSM]] — MENTION — n/a — implicated in sanctions circumvention via Sophgo; faces potential $1B+ fine and heightened export-control scrutiny that could disrupt its China-adjacent revenue
