---
type: source
title: "Interconnects 101"
tags: []
related: []
created: 2024-07-03
updated: 2024-07-03
authors: [citrini]
year: 2024
url: "https://www.citriniresearch.com/p/interconnects-101"
venue: Citrini Research
post_date: 2024-07-03
tickers: [NVDA, CRDO, MRVL, AVGO, ALAB, LITE]
---

[[citrini]] publishes "Interconnects 101" as the first in a series of Intra-Thematic AI Primers under the "Bits & Bottlenecks" banner — a technical and investment-oriented primer on the interconnect layer of AI datacenter infrastructure. The core argument is that as AI investment matures beyond the initial Phase 1 GPU buildout, the next layer of winners will be concentrated in the companies solving data movement bottlenecks: the cables, retimers, optical transceivers, and silicon photonics components that link GPU clusters together.

## Why Interconnects Matter

The piece begins with GPU architecture basics: GPUs dominate AI training and inference because of their massively parallel core design — thousands of smaller cores executing identical operations simultaneously — versus the handful of high-frequency cores in CPUs optimized for sequential logic. As a historical marker, NVIDIA's 2007 Tesla GPU shipped with 512 cores versus Intel's Xeon at 4 cores. As model sizes have grown, the ability to network thousands of GPUs together at high bandwidth and low latency has become the binding constraint. Raw compute is no longer the bottleneck; data movement is.

## Interconnect Technology Taxonomy

Citrini walks through the key technologies across the interconnect stack:
- **PCIe** (Peripheral Component Interconnect Express): the dominant CPU-to-GPU and chip-to-chip protocol inside servers.
- **NVLink / InfiniBand**: NVIDIA's proprietary high-speed scale-up and scale-out fabric, enabling multi-GPU pods.
- **Ethernet**: increasingly the protocol of choice for hyperscaler custom silicon clusters as an open alternative to InfiniBand.
- **Retimers and redrivers**: signal integrity components that clean and re-amplify electrical signals over copper at high data rates; Astera Labs (ALAB) and Credo (CRDO) are highlighted here.
- **Active Electrical Cables (AECs) and Active Optical Cables (AOCs)**: hybrid and optical cable assemblies replacing passive copper over longer rack-to-rack distances.
- **Silicon photonics / datacom transceivers**: optical components enabling terabit-scale bandwidth in and out of AI servers; Marvell (MRVL) is cited for pushing 400G-per-lane PAM technology enabling 3.2T optical links; Lumentum (LITE) surfaces as a components supplier beneficiary.

## Investment Thesis

Citrini's central call is that interconnects are **more insulated from the risk of AI datacenter capex moderation** than pure-play GPU suppliers because: (1) interconnect demand is amplified by custom silicon efforts — hyperscalers building their own ASICs (rather than buying NVIDIA GPUs) still need interconnect components, often in greater quantity; (2) inference workloads, which are growing faster than training, are more network-bandwidth-intensive relative to raw compute; and (3) the transition from copper to optical at ever-shorter reach is a secular multi-year upgrade cycle regardless of aggregate capex levels. NVIDIA (NVDA) is acknowledged as the "trusty Phase 1 AI beneficiary," but Citrini signals that the next phase will see more dispersion away from the handful of obvious names. Broadcom (AVGO) is mentioned as a broad AI semis and custom silicon participant.

## Key Data Points

- NVIDIA Tesla (2007): 512 cores. Intel Xeon (contemporaneous): 4 cores — illustrating the architectural divergence enabling GPU dominance.
- Marvell is cited as pushing 400G-per-lane PAM technology, enabling 3.2 Tbps optical interconnect modules.
- AI inference workloads are characterized as bandwidth-heavy relative to training, strengthening the interconnect thesis as the industry transitions from training-dominant to inference-dominant compute spend.

## Calls

- [[NVDA]] — LONG — n/a — Acknowledged Phase 1 AI beneficiary; less differentiated going forward but remains the GPU standard.
- [[CRDO]] — LONG — n/a — Top-ranked interconnect name; retimer and active electrical cable expertise directly addresses AI cluster bandwidth bottlenecks.
- [[MRVL]] — LONG — n/a — Pushing 400G-per-lane PAM optics enabling 3.2T interconnect modules; custom silicon and optical exposure.
- [[AVGO]] — LONG — n/a — Broad AI semis and custom silicon participant; benefits from hyperscaler ASIC spend driving interconnect demand.
- [[ALAB]] — LONG — n/a — Astera Labs; PCIe retimer and connectivity silicon for AI servers.
- [[LITE]] — LONG — n/a — Lumentum; optical components supplier benefiting from the silicon photonics and transceiver upgrade cycle.
