---
type: source
title: "100,000 H100 Clusters: Power, Network Topology, Ethernet vs InfiniBand, Reliability, Failures, Checkpointing"
tags: []
related: []
created: 2024-06-17
updated: 2024-06-17
authors: [semianalysis]
year: 2024
url: "https://newsletter.semianalysis.com/p/100000-h100-clusters-power-network"
venue: SemiAnalysis
post_date: 2024-06-17
tickers: [NVDA, AVGO, MSFT, META]
---

[[semianalysis]] analyzes the technical and economic challenges of deploying 100,000-GPU H100 training clusters, covering power infrastructure, network topology tradeoffs, reliability engineering, and competitive dynamics among Nvidia, Broadcom, and hyperscalers.

## Power and Scale

A 100,000 H100 cluster requires over 150 MW of critical IT power and consumes 1.59 terawatt-hours annually at an estimated cost of $123.9 million — exceeding the power draw of El Capitan (30 MW). Individual clusters represent more than $4 billion in server capex alone. At scale, a 100k H100 cluster could train a GPT-4-equivalent model in 4 days using FP8, versus 90–100 days on 20,000 A100s, making reliability and utilization paramount.

## Network Topology

Large clusters use "island" architectures with high internal bandwidth and deliberate oversubscription between islands. Meta's 32,000-GPU design uses 8 islands with 7:1 oversubscription at the top layer. Full fat-tree topologies are cost-prohibitive due to optical transceiver expenses. A key design choice is rail-optimized (Nvidia-recommended, each H100 connects to 8 different leaf switches, single-hop routing) versus middle-of-rack (leaf switches co-located with GPUs, using 98,304 fewer optical transceivers, cutting transceiver power from ~1,500 W optical to ~747 W copper DAC).

## InfiniBand vs. Ethernet vs. Broadcom

**Nvidia Quantum-2 InfiniBand**: 64 ports of 400G per switch, supports SHARP in-network reductions (theoretical 2x bandwidth improvement), but limited to 65,536 fully connected H100s, requiring a 4-tier topology for 100k clusters.

**Nvidia Spectrum-X Ethernet**: 128 ports of 400G enabling a 3-tier topology (33% fewer transceivers), but lacks SHARP and requires Bluefield-3 NICs adding ~400 W per node (~+5 MW cluster-wide). Uses proprietary Nvidia transceivers.

**Broadcom Tomahawk 5**: 128 ports of 400G, compatible with generic transceivers from multiple vendors, no proprietary NIC power penalty, lowest total cost at hyperscaler scale — but requires significant internal engineering to optimize NCCL collectives. SemiAnalysis predicts hyperscalers will increasingly adopt Tomahawk 5 as proprietary solutions impose unacceptable power and cost penalties.

## Reliability and Checkpointing

With a mean time to failure of 5 years per transceiver link, a 100k cluster experiences its first job failure in approximately 26.28 minutes without mitigation. Microsoft/OpenAI's Cedar-7 dual-port transceiver modules halve transceiver count to 49,152, extending mean time to first failure to 42.05 minutes. Recovery methods: (1) **Checkpoint restart** — saves weights to persistent storage but can lose up to 99 training steps (~229 GPU-days of compute); (2) **Memory reconstruction via RDMA** — copies weights between GPU HBM over the backend fabric in ~1.6 seconds, losing only 1 step (~4.1 GPU-days). Leading labs implement RDMA-based memory reconstruction; smaller operators rely on slower checkpoint methods. Nvidia's RAS engine performs chip-level failure prediction and pre-job self-checks.

## Calls

- [[NVDA]] — LONG — n/a — Dominant supplier of H100 GPUs and InfiniBand networking; proprietary stack (Quantum-2, Spectrum-X, ConnectX-7, SHARP) is deeply embedded in hyperscaler infrastructure, though power/cost penalties at 100k scale create long-term risk from Broadcom alternatives.
- [[AVGO]] — LONG — n/a — Broadcom Tomahawk 5 is the lowest-cost, most open network switch for 100k GPU clusters; hyperscalers with sufficient engineering resources are forecast to migrate toward it, expanding Broadcom's AI networking TAM.
- [[MSFT]] — MENTION — n/a — Microsoft/OpenAI's Cedar-7 transceiver innovation cited as leading-edge infrastructure engineering that meaningfully improves cluster reliability.
- [[META]] — MENTION — n/a — Meta's 32,000-GPU island architecture with 7:1 oversubscription is used as the canonical design reference for large-scale GPU cluster topology.
