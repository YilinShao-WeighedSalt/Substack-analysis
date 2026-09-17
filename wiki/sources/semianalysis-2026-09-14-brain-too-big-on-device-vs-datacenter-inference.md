---
type: source
title: "A Brain Too Big to Carry — On-Device vs Datacenter Inference"
tags: [robotics, embodied-ai, jetson, edge-inference, nvidia, tsmc, networking]
related: ["[[semianalysis]]", "[[NVDA]]", "[[robotics-embodied-ai]]", "[[nvidia-gpu-platform]]", "[[foundry-process-node]]"]
created: 2026-09-17
updated: 2026-09-17
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/a-brain-too-big-to-carry-on-device"
venue: SemiAnalysis
post_date: 2026-09-14
tickers: [NVDA]
---

Where should a robot's "brain" run — onboard or in a datacenter? A robotics/embodied-AI deep dive with no clean single ticker call (reinforces NVDA + TSMC advanced-node demand).

**The embodiment problem.** Robotics inverts the LLM playbook: hardware is fixed and the model is sized to fit real-time (100Hz+ control loops) and upfront per-unit cost. Frontier robot models stay small (π0 ~3B, π0.7 5B on an off-robot H100, GR-3 4B, Generalist ~10B, DreamZero 14B needs 2x GB200). Layers: **planning (≤20Hz, offloadable)** over **action/servo (100Hz+, must stay onboard)**. Jitter (not latency) is what blocks offloading the planner.

**Why the datacenter pulls the work.** Jetson Thor is ~1/10th a GB200's FLOPs and ~1/30th its memory bandwidth; off-robot compute escapes the power/compute budget and pools inference across a fleet. **Supply-chain reality:** robot silicon is converging onto the same leading-edge nodes as the datacenter (Orin SF8 → Thor N4 → next-gen N3 alongside Rubin → N2), Jetson is a thin sliver of Nvidia output at mid-60s% GM vs mid-to-high-70s for datacenter Blackwell, so Nvidia points scarce wafers at the datacenter and Jetson margins only inflect once robotics volume arrives. **The network wall:** offloading needs robot-aware access points (uplink scheduling, location-aware beamforming, centralized timing, multi-link WiFi/5G, 6GHz), a mainboard built for 4x4 uplink MIMO on one clock, and perception that shrinks the uplink load. Figure's BMW deployment (~1,250 hours over 11 months, ~40% util) is the anchor datapoint; industrial demand clears a higher bar than the home.

## Calls
- No priced ticker call. Thesis reinforces **[[NVDA]]** (Jetson + datacenter robot inference optionality) and TSMC leading-edge demand (→ [[robotics-embodied-ai]]).
