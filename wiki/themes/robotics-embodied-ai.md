---
type: theme
title: "Robotics & Embodied AI"
tags: []
related: []
created: 2024-06-03
updated: 2026-09-17
status: maturing
first_seen: 2024-06-03
---
## Timeline
- 2024-06-03 — [[citrini-2024-06-03-annual-review-ai-highlights]] (citrini)
- 2025-03-11 — [[semianalysis-2025-03-11-america-missing-new-labor-economy-robotics]] (semianalysis)
- 2025-03-11 — [[semianalysis-2025-03-11-america-missing-new-labor-economy-robotics]] (semianalysis)
- 2025-03-11 — [[semianalysis-2025-03-11-america-missing-new-labor-economy-robotics]] (semianalysis)
- 2025-07-21 — [[semianalysis-2025-07-21-intel-18a-dram-vlsi2025]] (semianalysis)
- 2025-07-30 — [[semianalysis-2025-07-30-robotics-levels-of-autonomy]] (semianalysis)
- 2025-07-30 — [[semianalysis-2025-07-30-robotics-levels-of-autonomy]] (semianalysis)
- 2025-07-30 — [[semianalysis-2025-07-30-robotics-levels-of-autonomy]] (semianalysis)
- 2025-07-30 — [[semianalysis-2025-07-30-robotics-levels-of-autonomy]] (semianalysis)
- 2025-07-30 — [[semianalysis-2025-07-30-robotics-levels-of-autonomy]] (semianalysis)
- 2025-09-18 — [[citrini-2025-09-18-single-stock-long-thesis]] (citrini)
- 2025-10-20 — [[semianalysis-2025-10-20-quadruped-state-market-unitree-boston-dynamics]] (semianalysis)
- 2025-10-20 — [[semianalysis-2025-10-20-quadruped-state-market-unitree-boston-dynamics]] (semianalysis)
- 2025-10-20 — [[semianalysis-2025-10-20-quadruped-state-market-unitree-boston-dynamics]] (semianalysis)
- 2025-10-20 — [[semianalysis-2025-10-20-quadruped-state-market-unitree-boston-dynamics]] (semianalysis)
- 2026-03-18 — [[globalsemiresearch-2026-03-18-chinese-openclaw-tech-frenzy-rationality]] (globalsemiresearch)
- 2026-06-03 — [[semianalysis-2026-06-03-case-for-space-datacenters]] (semianalysis)
- 2026-06-03 — [[semianalysis-2026-06-03-case-for-space-datacenters]] (semianalysis)
- 2026-06-08 — [[semianalysis-2026-06-08-unitree-dominate-global-robotics]] (semianalysis)
- 2026-06-08 — [[semianalysis-2026-06-08-unitree-dominate-global-robotics]] (semianalysis)
- 2026-06-08 — [[semianalysis-2026-06-08-unitree-dominate-global-robotics]] (semianalysis)
- 2026-06-08 — [[semianalysis-2026-06-08-unitree-dominate-global-robotics]] (semianalysis)

## Narrative
Citrini first flagged robotics and embodied AI as a meaningful theme in mid-2024 within a broader AI highlights review, but SemiAnalysis drove the bulk of analytical depth beginning in early 2025 with a multi-part examination of how robotics intersects with America's labor economy. Coverage accelerated sharply through 2025: SemiAnalysis mapped out levels of autonomy for robotic systems in July, then conducted a detailed competitive teardown of the quadruped market — Unitree versus Boston Dynamics — in October, establishing a clear framework for evaluating the Chinese versus US hardware stack. By early 2026, GlobalSemiResearch added a critical lens on Chinese openclaw technology and market rationality, while SemiAnalysis's June 2026 deep-dive on Unitree's global robotics dominance marks the most concentrated single-source coverage yet. The theme has moved from early-stage AI-adjacent interest to a maturing area of serious competitive and supply-chain analysis, with Unitree emerging as the central subject and Chinese manufacturing capability as the defining structural tension.


## Update 2026-09-17 — where the robot's brain runs (SemiAnalysis, "A Brain Too Big to Carry")
Plain-language model of embodied inference. **Robotics inverts the LLM playbook:** hardware is fixed and models are sized to fit real-time deadlines and per-unit cost (paid upfront on every robot), so frontier robot models stay small (billions of params: π0 ~3B, DreamZero 14B needs 2x GB200) vs trillion-param LLMs. **Layer stack:** a *planning* layer (≤20Hz — slow enough to offload to a datacenter GPU) sits over *action/servo* loops (100Hz+ — must stay onboard because a wireless round-trip alone eats the 10ms budget). **Jitter, not latency, is the real blocker** to offloading the planner. **Why the datacenter pulls the work:** Jetson Thor is ~1/10th a GB200's FLOPs / ~1/30th its bandwidth; off-robot compute escapes the power budget and pools inference across a fleet. **Supply-chain reality:** robot silicon is converging onto the datacenter's leading-edge nodes (Orin SF8 → Thor N4 → N3 with Rubin → N2), and since Jetson earns mid-60s% GM vs mid-to-high-70s for datacenter Blackwell, Nvidia starves edge silicon of scarce wafers until robotics volume arrives (then Jetson margins inflect). **The "network wall"** (the gating problem for off-device robots): robot-aware uplink scheduling, location-aware beamforming, one shared clock, multi-link WiFi/5G, clean 6GHz spectrum, and 4x4-uplink-MIMO mainboards co-designed with the access point. Investable read: reinforces NVDA (Jetson + datacenter) and TSMC advanced-node demand; no clean standalone robotics ticker yet.
