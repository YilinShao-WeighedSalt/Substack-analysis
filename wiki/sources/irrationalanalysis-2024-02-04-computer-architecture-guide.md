---
type: source
title: "A Guide on Computer Architecture"
tags: []
related: []
created: 2024-02-04
updated: 2024-02-04
authors: [irrationalanalysis]
year: 2024
url: "https://irrationalanalysis.substack.com/p/a-guide-on-computer-architecture"
venue: Irrational Analysis
post_date: 2024-02-04
tickers: [NVDA, AMD, INTC]
---

[[irrationalanalysis]] provides a taxonomy of chip designs — CPU, GPU, ASIC, and Exotic — framed explicitly for investors trying to understand the AI hardware boom.

**CPUs** are built around von Neumann architecture and excel at "branchy" general-purpose code through three costly features: branch prediction, out-of-order execution, and speculative execution. These features consume substantial transistor area and power versus more specialized designs, making CPUs the flexible but inefficient generalist. The analogy used is a team of ten domain experts — each capable across many tasks, but hard to coordinate efficiently.

**GPUs** operate on waves/warps (groups of ~32 numbers processed simultaneously), making them purpose-built for the linear-algebra-heavy workloads that underpin both graphics and AI. NVDA uses warp32 with a software-defined scheduler that places more burden on the host CPU; AMD previously used wave64 (noted as a failure) and has since moved to wave32 for gaming; Qualcomm uses variable-length waves optimized for power/area; Intel GPU efforts are dismissed outright as "Dead." The author emphasizes that CUDA is central to NVDA's competitive moat — GPU programming is painful, and CUDA abstracts that complexity so AI/ML researchers can write Python and get near-metal performance. This software layer is positioned as a durable, hard-to-replicate advantage.

**ASICs** are purpose-built blocks that handle one task (video encode/decode, cryptography, etc.) with extreme efficiency but zero flexibility. Examples cited include Apple's M-series media engine and Intel's Quick Assist on Sapphire Rapids. The framing is that ASICs destroy CPUs and GPUs on their specific task but are useless outside it.

**Exotic** architectures include VLIW designs and outliers like the Cerebras Wafer-Scale Engine, Lightmatter (optical compute), and the notoriously difficult Cell Broadband Engine (PS3). These sit outside the CPU/GPU/ASIC boxes and are flagged as interesting but hard to program.

The investment-relevant conclusion is implicit: GPU/CUDA dominance (NVDA) is durable because of software lock-in; AMD is a distant second; Intel's GPU effort is effectively written off.

## Calls

- [[NVDA]] — LONG — px@n/a — CUDA software moat makes NVDA the dominant beneficiary of AI GPU demand, with a hard-to-replicate middleware layer locking in AI/ML researchers
- [[AMD]] — NEUTRAL — px@n/a — Second-tier GPU vendor, previous wave64 misstep noted, now converging on wave32; capable but lacking NVDA's software ecosystem
- [[INTC]] — SHORT — px@n/a — Intel's GPU effort dismissed as "Dead" with no viable path to relevance in the AI accelerator market
