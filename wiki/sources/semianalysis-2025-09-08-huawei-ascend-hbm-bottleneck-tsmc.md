---
type: source
title: "Huawei Ascend Production Ramp: Die Banks, TSMC Continued Production, HBM is The Bottleneck"
tags: []
related: []
created: 2025-09-08
updated: 2025-09-08
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/huawei-ascend-production-ramp"
venue: SemiAnalysis
post_date: 2025-09-08
tickers: [NVDA, MU, ASML]
---
[[semianalysis]] (Dylan Patel, AJ Kourabi, Myron Xie) dissects the true constraints on Huawei's Ascend AI chip production ramp, concluding that HBM supply — not logic die fabrication capacity — is the binding bottleneck preventing China from scaling past 805k units in 2025.

**Production numbers and die banks.** Huawei shipped 507k Ascend units in 2024 and is on track for 805k in 2025, with 653k being the advanced 910C model. Critically, more than 2.9 million Ascend die were sourced from TSMC through a "die bank" mechanism before export controls tightened, providing a substantial stockpile. SMIC currently operates at ~45k wafers per month (wspm) at 7nm-class, scaling to 60k wspm in 2026 and 80k wspm by 2027 — but Ascend only requires ~20k wspm of that allocation, meaning logic die is not scarce.

**HBM is the bottleneck.** China's own behavior confirms this: during trade negotiations Beijing requested relaxation of HBM controls, but did not request relief on TSMC access or lithography equipment. Samsung exported roughly 11.4 million HBM stacks to China, including a staggering 7 million stacks in the one-month gap between the U.S. controls announcement and enforcement. Total foreign HBM stockpile is ~13 million stacks, enough for ~1.6 million Ascend 910C packages. Domestic CXMT can only produce ~2 million HBM stacks per year at current capacity, covering just 250k–300k Ascends annually. The authors state plainly: "China can easily make more than 805k Huawei Ascends this year from TSMC and SMIC capacity, but they will not because they do not have enough HBM."

**CXMT and domestic DRAM ramp.** CXMT is rapidly scaling DRAM production with CCP "Big Fund III" backing ($2B injected May 2024) and aggressive equipment stockpiling. By 2026 it may reach ~257k wspm (roughly 15% of global DRAM capacity). Even in an optimistic scenario where CXMT diverts half its capacity to HBM, domestic supply could enable 5+ million Ascends annually — making enforcement against CXMT urgent.

**Nvidia H20 and B30A.** The U.S. approved Nvidia H20 exports to China, providing a compute buffer. More concerning, a proposed Blackwell B30A variant could deliver more than 10x the FLOPs of the H20 at equivalent memory bandwidth, which the authors warn would materially accelerate Chinese AI development. They argue the U.S. should not raise the capability bar of chips exported to China until China can ship something competitive to the H20 at scale.

**Enforcement gaps.** HBM smuggling via CoAsia Electronics and Faraday Technology (non-functional chip shipments) has been documented. Huawei continues to access TSMC for networking chips and datacenter CPUs through shell companies. ASML's NXT:1980 lithography tools remain accessible to China and are sufficient for 7nm-class production. The authors call for immediate entity-listing of CXMT, tighter allied coordination on control timelines, and enforcement on Chinese OSATs packaging HBM.

## Calls

- [[NVDA]] — MENTION — n/a — H20 approved for China export providing compute buffer; proposed B30A variant flagged as potentially excessive capability concession
- [[MU]] — MENTION — n/a — cited alongside Samsung and SK Hynix as foreign HBM suppliers whose exports to China are the critical enforcement target
- [[ASML]] — MENTION — n/a — NXT:1980 tools accessible to China and sufficient for 7nm-class logic production, cited as a gap in Western export control coordination
