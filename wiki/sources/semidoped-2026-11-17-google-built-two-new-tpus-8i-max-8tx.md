---
type: source
title: "SD Episode — Google Built Two New TPUs Without New Silicon: The 8i Max and 8TX"
tags: []
related: ["[[semidoped]]", "[[GOOGL]]", "[[AMD]]", "[[custom-silicon-asic]]"]
created: 2026-11-19
updated: 2026-11-19
authors: [semidoped]
year: 2026
url: "https://daily.semidoped.com/p/new-episode-google-built-two-new"
venue: Semi Doped
post_date: 2026-11-17
tickers: [GOOGL, AMD]
---

Educational episode (recorded Nov-12). Google announced **two more V8-generation TPU systems — not new silicon — the 8TX and 8i Max**, joining the earlier **8T (training)** and **8i (inference)**, giving **four flavors of one generation**. Refresher: the 8i (inference) has **more HBM (288 GB vs 216) and ~3× the on-chip SRAM (384 MB)** than the 8T and is physically the *bigger* die — inference is the memory-bound problem. The **8i Max** doubles down on memory for inference (memory-maxed). The **8TX** is a **confidential-computing** variant pairing the TPU with an **AMD EPYC host CPU** (secure enclave) — notable because Google chose AMD for the secure host socket; the hosts also mix a training-silicon core (8T) with an inference network (Boardfly), a deliberate mismatch the hosts debate. **TPU Sync** is Google's inference-orchestration software layer — explicitly framed as **Google's answer to Nvidia's Dynamo** — and a step toward **selling TPUs to external customers** (the business-strategy thread: order visibility to 2029 via OpenAI/Anthropic interest). Deepens [[custom-silicon-asic]] concept knowledge: four-SKU-per-generation strategy, SRAM/HBM memory-hierarchy choices, Boardfly topology, confidential-compute-with-EPYC, TPU-Sync-vs-Dynamo.

## Calls
- **[[GOOGL]] LONG — $280.20** (px@call Nov-18 close): four V8 TPU SKUs (8TX/8i Max) + TPU Sync (Dynamo rival) + external-customer push; combined with Nov-16 chatter (TPU visibility to 2029, buying HBM direct).
- **[[AMD]] — context**: chosen as the secure EPYC host inside TPU 8TX (reinforces the AMD host-CPU thesis; priced under the Nov-17 daily).
