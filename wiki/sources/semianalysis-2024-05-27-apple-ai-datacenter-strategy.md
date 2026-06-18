---
type: source
title: "Apple's AI Strategy: Apple Datacenters, On-device, Cloud, And More"
tags: []
related: []
created: 2024-05-27
updated: 2024-05-27
authors: [semianalysis]
year: 2024
url: "https://newsletter.semianalysis.com/p/apples-ai-strategy-apple-datacenters"
venue: SemiAnalysis
post_date: 2024-05-27
tickers: [AAPL, TSM, NVDA]
---

Written by Dylan Patel and Myron Xie at [[semianalysis]], this piece lays out Apple's three-tier AI infrastructure strategy ahead of WWDC 2024 and the iOS 18 launch.

## Summary

The central puzzle the authors pose is why Apple is ramping M2 Ultra chip production to record volumes in 2024 when consumer demand for the Mac Studio and Mac Pro — the only products that use the M2 Ultra — does not justify the increase. The M3 Ultra was quietly cancelled, deepening the mystery. The answer, they argue, is that Apple intends to deploy these chips inside its own datacenters to serve AI workloads for iOS 18 features, rather than relying on external GPU cloud providers.

**Datacenter buildout.** SemiAnalysis's internal tracking identifies seven Apple datacenter sites containing over 30 buildings in total. Apple is on pace to roughly double its total datacenter capacity in the near term, with its largest campus set to add several new facilities. This is a meaningful infrastructure commitment by a company that has historically leaned on third-party cloud.

**Chip strategy.** The M2 Ultra is assembled by bonding two M2 Max dies using TSMC's InFO-LSI packaging technology — an approach analogous to (but distinct from) Nvidia's CoWoS-L used in Blackwell. Apple's use of proprietary server silicon lets it control cost, performance-per-watt, and data privacy in a way GPU-based cloud cannot.

**GPU purchasing.** Despite the AI GPU boom, Apple ranks outside the top 10 purchasers of Nvidia GPUs according to SemiAnalysis's Accelerator Model. This signals a deliberate strategic choice to route AI compute through Apple silicon rather than Nvidia accelerators.

**Key hire.** Apple recruited Sumit Gupta in March 2024 to lead cloud infrastructure. Gupta spent 2007–2015 at Nvidia and then moved to Google, where he managed TPU and Arm-based datacenter CPU products — exactly the background needed to build out proprietary AI server infrastructure.

**OpenAI partnership.** Apple is simultaneously partnering with OpenAI for tasks that exceed on-device capability. The authors note the deal economics are unusual — they describe the dynamic relative to Apple's ~$20B Google search deal but indicate the OpenAI arrangement works differently, without disclosing specific terms. The net architecture is: simple tasks run on-device (Neural Engine), medium tasks hit Apple's own M2 Ultra servers, and complex or sensitive queries route to OpenAI.

**Investment implications.** The strategy is constructive for Apple's long-term AI margin profile (avoids per-query GPU cloud costs, preserves privacy as a differentiator) and is a clear negative read-through for Nvidia's addressable market at Apple — one of the world's largest device ecosystems is explicitly not buying H100s. TSMC benefits as the packaging and process node supplier for Apple's datacenter silicon.

## Calls

- [[AAPL]] — LONG — n/a — proprietary M2 Ultra server ramp and three-tier AI architecture positions Apple to deliver iOS 18 AI features with controlled cost and privacy advantages
- [[TSM]] — LONG — n/a — sole supplier of Apple's InFO-LSI packaged M2 Ultra datacenter chips; benefits from Apple's accelerating server silicon ramp
- [[NVDA]] — MENTION — n/a — Apple is explicitly not a top-10 Nvidia GPU buyer despite industry-wide AI demand, illustrating limits of Nvidia's TAM at major hyperscaler-like customers who build proprietary silicon
