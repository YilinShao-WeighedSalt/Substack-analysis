---
type: source
title: "Nvidia's Optical Boogeyman NVL72, Infiniband Scale Out, 800G & 1.6T Ramp"
tags: []
related: []
created: 2024-03-25
updated: 2024-03-25
authors: [semianalysis]
year: 2024
url: "https://newsletter.semianalysis.com/p/nvidias-optical-boogeyman-nvl72-infiniband"
venue: SemiAnalysis
post_date: 2024-03-25
tickers: [NVDA, COHR, LITE, MRVL]
---

[[semianalysis]] argues that the market panic around Nvidia's DGX GB200 NVL72 rack announcement at GTC 2024 — specifically Jensen Huang's claim that NVLink copper cables saved 20 kilowatts of optical transceiver power — is a misread of the system architecture. The NVL72 does eliminate optical transceivers from the intra-rack scale-up (NVLink) domain, but the scale-out backend network (InfiniBand or Ethernet) still requires exactly one optical NIC per GPU, identical to H100 cluster deployments. Optical transceiver volumes therefore scale linearly with GPU cluster growth regardless of NVLink copper adoption.

**NVL72 architecture:**

The integrated rack houses 72 Hopper-successor GPUs, 36 Grace CPUs, 18 NVSwitches, 72 InfiniBand NICs, 36 BlueField 3 Ethernet NICs, and 5,184 direct-drive copper NVLink cables providing 900 GB/s per GPU within the rack. The 72 OSFP ports at 400G/800G — one per GPU — service the backend scale-out network and remain fully populated in any real deployment. No customer deploys a single rack in isolation; multi-rack scale-out is universal, keeping optical port counts high.

**InfiniBand scale-out and 800G/1.6T ramp:**

At scale, each GPU requires one 400G or 800G OSFP transceiver for InfiniBand or Ethernet connectivity. As clusters grow from thousands to tens of thousands of GPUs across hyperscaler and neocloud deployments, the transceiver bill grows proportionally. The 800G OSFP cycle is actively ramping in 2024, driven by NVL72 and H100/H200 cluster refreshes, with 1.6T (2x800G or DR8 configurations) on the horizon for 2025 deployments. Coherent, Lumentum, and Marvell (for DSP/retimer silicon) are primary beneficiaries of this ramp.

**The real optical boogeyman:**

The article explicitly teases an unnamed future technology — distinct from NVL72 copper NVLink — as the genuine structural threat to discrete optical transceiver volumes. This is a forward warning about co-packaged optics (CPO) or next-generation integrated photonics approaches that could displace pluggable transceiver modules, expected to become material around 2025-2026. The post does not name specific companies at risk but implies pluggable transceiver vendors face structural disruption longer-term.

**Implications for optical supply chain:**

Near-term (2024-2025), demand for 400G/800G pluggable transceivers is robust and unimpacted by NVL72 copper NVLink. The optical TAM expands with GPU cluster scale-out. Longer-term, the CPO/integrated photonics transition poses a secular risk to COHR and LITE.

## Calls

- [[NVDA]] — LONG — n/a — NVL72 copper NVLink is a power efficiency win that does not reduce optical TAM; Nvidia's AI cluster dominance drives transceiver volume growth
- [[COHR]] — LONG — n/a — 800G/1.6T pluggable transceiver ramp is intact; near-term demand driven by InfiniBand scale-out per the NVL72 architecture
- [[LITE]] — LONG — n/a — Lumentum benefits from same 800G optical ramp; NVL72 copper scare overstated, pluggable demand resilient through 2025
- [[MRVL]] — LONG — n/a — Marvell DSP and retimer silicon required for 800G/1.6T optical transceivers; scales with backend InfiniBand NIC attach rate
