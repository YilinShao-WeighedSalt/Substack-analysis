---
type: source
title: "SemiAnalysis — The Huawei–DeepSeek Symbiosis"
tags: [geopolitics-export-controls, ai-accelerator-competition, hbm-memory]
related: ["[[semianalysis]]", "[[NVDA]]", "[[geopolitics-export-controls]]", "[[ai-accelerator-competition]]", "[[hbm-memory]]"]
created: 2026-10-23
updated: 2026-10-23
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/huawei-deepseek"
venue: SemiAnalysis
post_date: 2026-10-21
tickers: [NVDA]
---

Technical deep-dive (full body served), **no priced ticker call** — ingested as domain knowledge.

Thesis: **Huawei + DeepSeek form a symbiotic, vertically-integrating Chinese AI stack.** Neither can do it alone — Huawei has silicon (Ascend) but no frontier lab to prove it trains/infers; DeepSeek has models but can't buy the compute it needs. DeepSeek's Sep-30 release of **Ascend support for TileLang, DeepGEMM, DeepEP, TileKernels, FlashMLA, DeepSelect** is the artifact of that trade (the exchange runs "through the kernel-authoring language"). SA expects DeepSeek to be primarily on Huawei's stack by 2027-28.

Key technical findings (**Ascend 950PR**, 28 cube cores / 128GiB HBM):
- Huawei **bins both compute *and* memory into multiple SKUs** (pairs weak dies with weak HBM), unlike Nvidia which bins compute only — a response to defects + parametric shortfalls.
- Contains **Linx816 AArch64 AICPUs** (Kirin-9000S-class middle cores) for short/overhead-dominated work (KV metadata, DSA index selection).
- **GEMM:** Huawei's best kernels hit **99.7% of ceiling** (DeepSeek's DeepGEMM isn't the only path); but absolute perf sits **between A100 and MI300X** — hardware "~5 years behind A100," **software right at the frontier**.
- **MemBW:** 950PR's effective bandwidth/utilization surpasses H100 at small message sizes.
- Co-design runs both ways: FlashMLA KV layout rewritten to co-locate values+scales (fewer MTE transfers); **DeepEP-Ascend** (port of DeepEP V2.5 over URMA/HCCL) lives under DeepSeek's org after a DeepEP maintainer declined Huawei's PR.
- **DSv4.1-Flash** is the first DeepSeek model to use **Engram** (async token-ID fetch overlaps layer-0 compute → DRAM-offload with no perf loss vs HBM, but PCIe-4.0 SSD degrades).
- Caveat: optimizations are supernode/ARM-centric — **vLLM-Ascend barely works on x86 hosts** (no DeepGEMM, hardcoded ARM headers), so the partnership helps DeepSeek more than the broader ecosystem.

Read-through: reinforces the slow erosion of the **CUDA moat** inside China and the 4-hi-HBM/DRAM-offload memory arc; near-term China still buys Nvidia (ByteDance/Alibaba/Tencent >$35B orders this same week). → **[[NVDA]]** (long-term China-share headwind, no fresh priced call), [[geopolitics-export-controls]], [[ai-accelerator-competition]], [[hbm-memory]].

## Calls
- None priced (all private: Huawei, DeepSeek).
