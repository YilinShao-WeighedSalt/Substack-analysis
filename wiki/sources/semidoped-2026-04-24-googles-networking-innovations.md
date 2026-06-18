---
type: source
title: "Google's Networking Innovations"
tags: []
related: []
created: 2026-04-24
updated: 2026-04-24
authors: [semidoped]
year: 2026
url: "https://www.semidoped.com/p/googles-networking-innovations"
venue: Semi Doped
post_date: 2026-04-24
tickers: [LITE, COHR]
---

[[semidoped]] breaks down Google's Cloud Next 2026 announcements, focusing on a fundamental architectural shift in how the company designs hardware and networking for AI workloads — moving decisively away from general-purpose silicon toward extreme co-design between compute and interconnect.

## Dual TPU Strategy

Google introduced two distinct TPU v8 variants for different workloads. The TPU 8T (training) carries 216 GB HBM and 128 MB SRAM, while the TPU 8I (inference) prioritizes memory bandwidth with 288 GB HBM and 384 MB SRAM — three times the on-chip SRAM of the training chip. Both variants use ARM-based Axion CPUs as head nodes, eliminating data preparation bottlenecks that previously forced CPU-to-accelerator synchronization overhead.

## Virgo: Scale-Out Network Replaces Jupiter

Google retired its Jupiter datacenter fabric (designed in the internet era, 2015–2023) with Virgo, a ground-up redesign for AI. Aggregate bandwidth jumps from 13.1 petabits/second to 47 petabits/second (~3.6x). Virgo uses optical circuit switching (OCS) exclusively and collapses the traditional multi-layer Clos topology to just two layers, enabling a "campus as a computer" model that connects 134,000 TPUs with minimal hop counts. OCS vendors Lumentum (LITE) and Coherent (COHR) are named as integral suppliers of the switching hardware underpinning this architecture.

## Scale-Up Networks: Two Separate Topologies

For training, Google retains a 3D Torus topology (analogous to a Rubik's Cube), using copper PCB for neighbor connections and optical for distant links in an 8×8×16 configuration requiring up to 16 hops. For MoE inference, Google introduced Boardfly: a three-tier hierarchy (boards of 4 TPUs → groups of 8 boards → pods of 36 groups via OCS), totaling 1,152 TPUs per pod and cutting maximum hop count from 16 to 7 — more than a 50% latency reduction.

## Accelerating Collectives

TPU Direct RDMA enables direct memory access between TPUs without host CPU intermediaries, reducing coherency latency. The Collective Acceleration Engine (CAE) offloads all-reduce, all-gather, and all-to-all operations — analogous to NVIDIA's (NVDA) SHARP technology — freeing TPU compute from communication overhead.

## Strategic Implications

The overarching thesis is that the industry has crossed a threshold where workload-specific silicon and co-designed interconnect are now table stakes for competitive AI infrastructure. The post leaves open questions about whether AWS Trainium and other hyperscaler ASICs will converge on similar workload-bifurcated approaches, and whether agentic and world-model workloads will demand yet another round of architectural reinvention.

## Calls

- [[LITE]] — MENTION — px@call n/a — Lumentum named as OCS switch supplier integral to Google's Virgo scale-out network
- [[COHR]] — MENTION — px@call n/a — Coherent named alongside Lumentum as a key OCS hardware vendor for Virgo
