---
type: source
title: "Multi-Datacenter Training: OpenAI's Ambitious Plan To Beat Google's Infrastructure"
tags: []
related: []
created: 2024-09-04
updated: 2024-09-04
authors: [semianalysis]
year: 2024
url: "https://newsletter.semianalysis.com/p/multi-datacenter-training-openais"
venue: SemiAnalysis
post_date: 2024-09-04
tickers: [NVDA, GOOGL, MSFT, CIEN, NOK, COHR, LITE, FN, MRVL]
---

[[semianalysis]] argues that as AI training clusters scale beyond 100,000 GPUs, physical constraints — construction lead times, permitting, and power availability — make single-datacenter training architecturally infeasible, forcing the industry toward multi-datacenter training. Google currently holds a decisive infrastructure lead built over more than a decade, but OpenAI and Microsoft are executing plans to match or surpass it at gigawatt scale.

**Google's Infrastructure Lead.** Google has deployed millions of liquid-cooled TPUs representing more than 1 GW of capacity, with individual datacenter PUE of 1.1 (2023). Its Iowa/Nebraska clusters already exceed 500 MW and are expanding toward 1 GW by 2026. Critically, Google's Pathways software stack and Borg scheduler were purpose-built for multi-datacenter training and handle fault-tolerance corner cases through vertical integration that competitors cannot easily replicate.

**Microsoft/OpenAI Buildout.** Microsoft's Wisconsin campus will exceed all of Google's Ohio sites combined. Microsoft is partnering with Oracle, Crusoe, CoreWeave, QTS, Compass, and others to assemble multi-GW distributed capacity. However, Microsoft's current clusters show ~35% lower IT capacity per building than comparable Google facilities, with published PUE of 1.223 versus Google's 1.1.

**Core Technical Challenges.** Synchronous gradient descent across geographically separated sites imposes strict latency requirements (43.2 ms round-trip coast-to-coast at light speed). Stragglers are catastrophic: ByteDance experienced a 25% model flop utilization (MFU) decrease when stragglers accumulated across a large cluster, equivalent to 250,000 idle GPUs. Silent data corruption (SDC) — where undetectable errors distort outputs or produce NaN values — is another unresolved hazard; DCGMI Diagnostics misses corner cases such as NVSwitch ALU failures.

**Proposed Solutions.** The article outlines two complementary approaches. Hierarchical synchronous SGD creates latency tiers — frequent synchronization between buildings within 1 km, less frequent between regional sites within 100 km, minimal between distant regions — reducing straggler impact. An asynchronous parameter server approach (reviving Jeff Dean's 2012 DistBelief architecture) allows regional model replicas to work semi-independently, periodically merging weights like distributed version control. Training jobs at "100T+" parameters may require 5 Pbit/s intra-regional and 1 Pbit/s inter-regional bandwidth; exchanging 400 TB of weights at 5 Pbit/s takes 0.64 seconds.

**Telecom Networking as the Key Enabler.** Linking multi-datacenter clusters requires telecom-grade datacenter interconnect (DCI) rather than standard datacom optics. DWDM across C-band and L-band can deliver ~121.6 Tbps per fiber pair using DP-16QAM or DP-64QAM modulation — versus 400–800 Gbps per GPU on the datacom side. The article identifies telecom equipment and component suppliers as direct supply chain winners from this build-out, noting that non-cloud telecom demand appears to have bottomed and may be entering recovery, adding upside beyond the AI-driven DCI wave.

**Supply Chain Winners.** Systems vendors named: Ciena, Nokia, Infinera, Cisco. Component/subsystem vendors: Lumentum, Coherent, Fabrinet, Marvell. These companies benefit from the shift to higher-ASP telecom equipment and the surge in ZR/ZR+ pluggable optics demand for short-haul DCI.

## Calls

- [[NVDA]] — MENTION — n/a — dominant GPU supplier whose NVSwitch fabric faces reliability gaps (SDC corner cases) versus Google's vertically integrated TPU stack; not a negative call but a flagged infrastructure risk
- [[GOOGL]] — LONG — n/a — holds decisive multi-datacenter training lead via Pathways, Borg, and decade-plus TPU/liquid-cooling infrastructure; Microsoft/OpenAI may take years to close the gap
- [[MSFT]] — MENTION — n/a — executing aggressive multi-GW buildout alongside OpenAI but currently trails Google on PUE, per-building IT density, and software fault-tolerance
- [[CIEN]] — LONG — n/a — named telecom systems supplier benefiting from DCI upgrade cycle driven by multi-datacenter AI training bandwidth requirements
- [[NOK]] — LONG — n/a — named telecom systems supplier (also absorbed Infinera) positioned for higher-ASP DWDM/ROADM deployments as hyperscalers build out long-haul DCI
- [[COHR]] — LONG — n/a — named component/subsystem supplier for ZR/ZR+ and coherent optics underpinning multi-datacenter interconnect
- [[LITE]] — LONG — n/a — named component supplier for coherent optics and transceiver modules central to DCI build-out
- [[FN]] — LONG — n/a — named manufacturing partner for optical subsystems; benefits from volume ramp in ZR/ZR+ and higher-ASP telecom components
- [[MRVL]] — LONG — n/a — named subsystem supplier for coherent DSPs and networking silicon enabling high-baud-rate DCI links
