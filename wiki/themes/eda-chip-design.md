---
type: theme
title: "EDA & Chip Design Tools"
tags: []
related: []
created: 2024-01-11
updated: 2026-09-05
status: maturing
first_seen: 2024-01-11
---
## Timeline
- 2024-01-11 — [[semianalysis-2024-01-11-neural-network-quantization-number-formats]] (semianalysis)
- 2024-01-11 — [[semianalysis-2024-01-11-neural-network-quantization-number-formats]] (semianalysis)
- 2024-02-24 — [[irrationalanalysis-2024-02-24-very-long-incoherent-writeup]] (irrationalanalysis)
- 2024-03-16 — [[semianalysis-2024-03-16-cxl-is-dead-ai-era]] (semianalysis)
- 2024-09-02 — [[irrationalanalysis-2024-09-02-hot-chips-2024-irrational-recap]] (irrationalanalysis)
- 2024-09-22 — [[irrationalanalysis-2024-09-22-qualcomm-should-not-buy-intel]] (irrationalanalysis)
- 2025-01-24 — [[irrationalanalysis-2025-01-24-pdk-guide-semiconductors]] (irrationalanalysis)
- 2025-03-19 — [[semianalysis-2025-03-19-nvidia-gtc-vera-rubin]] (semianalysis)
- 2025-03-22 — [[irrationalanalysis-2025-03-22-tales-from-gtc-week]] (irrationalanalysis)
- 2025-05-17 — [[irrationalanalysis-2025-05-17-smh-favorite-names-q2-2025]] (irrationalanalysis)
- 2025-09-10 — [[irrationalanalysis-2025-09-10-masas-rocket-merry-go-round]] (irrationalanalysis)
- 2025-09-13 — [[irrationalanalysis-2025-09-13-synopsys-is-probably-buy]] (irrationalanalysis)
- 2025-09-13 — [[irrationalanalysis-2025-09-13-synopsys-is-probably-buy]] (irrationalanalysis)
- 2025-09-13 — [[irrationalanalysis-2025-09-13-synopsys-is-probably-buy]] (irrationalanalysis)
- 2025-12-24 — [[irrationalanalysis-2025-12-24-nvidia-groq-deal]] (irrationalanalysis)
- 2026-02-25 — [[semianalysis-2026-02-25-vera-rubin-extreme-co-design]] (semianalysis)
- 2026-02-27 — [[irrationalanalysis-2026-02-27-its-the-dataflow-stupid]] (irrationalanalysis)
- 2026-02-27 — [[irrationalanalysis-2026-02-27-its-the-dataflow-stupid]] (irrationalanalysis)
- 2026-03-31 — [[semianalysis-2026-03-31-blackwell-tensor-cores-ptx-sass]] (semianalysis)
- 2026-04-10 — [[globalsemiresearch-2026-04-10-cxl-ai-era-revolution-hype]] (globalsemiresearch)
- 2026-05-12 — [[semianalysis-2026-05-12-eda-primer-rtl-silicon]] (semianalysis)
- 2026-05-12 — [[semianalysis-2026-05-12-eda-primer-rtl-silicon]] (semianalysis)
- 2026-05-12 — [[semianalysis-2026-05-12-eda-primer-rtl-silicon]] (semianalysis)
- 2026-05-12 — [[semianalysis-2026-05-12-eda-primer-rtl-silicon]] (semianalysis)
- 2026-05-12 — [[semianalysis-2026-05-12-eda-primer-rtl-silicon]] (semianalysis)
- 2026-05-21 — [[semianalysis-2026-05-21-eda-market-cadence-synopsys-siemens]] (semianalysis)
- 2026-05-21 — [[semianalysis-2026-05-21-eda-market-cadence-synopsys-siemens]] (semianalysis)
- 2026-05-29 — [[semidoped-2026-05-29-huawei-tau-scaling-euv-killer-real]] (semidoped)

## Narrative
EDA and chip design tools emerged as a peripheral topic in early 2024, initially surfacing through quantization and number-format discussions tied to AI silicon, before irrationalanalysis began probing PDK fundamentals and the competitive dynamics around Intel's foundry decline in 2025. SemiAnalysis catalyzed a step-change in coverage density with a multi-part EDA primer in May 2026, followed immediately by a dedicated market analysis of Cadence, Synopsys, and Siemens — signaling the theme had crossed from background context into an investable thesis in its own right. The September 2025 cluster of Synopsys coverage by irrationalanalysis foreshadowed this shift, framing EDA vendors as direct beneficiaries of the AI-driven custom silicon boom. As of late May 2026, coverage spans the full stack from RTL-to-silicon flows and PDK access to competitive EDA vendor positioning, with semidoped adding a geopolitical angle via Huawei's TAU scaling efforts. The theme is maturing rapidly: breadth and depth of analysis are both expanding, but it has not yet reached the saturation level of established themes like HBM or NVIDIA GPU.

### 2026-08-27 — Synopsys beat/raise on the custom-ASIC wave
- **[[SNPS|Synopsys]] Q3 rev $2.477B / GAAP EPS $2.84** beat and **raised FY2026 guide**. The tell: accelerating **hyperscaler custom-ASIC + chiplet adoption** front-loads intensive **front-end EDA** work before every tapeout — the same AI-accelerated design cycle (Codex-written kernels, ~9-mo tapeouts) that makes labs like OpenAI viable chip designers is a *demand* pull for EDA franchises, not a threat.

### 2026-09-05 — OpenAI "Compilers 2.0": the LLM as a stochastic kernel optimizer
- Chris Leary (founder of Google's XLA compiler, now on OpenAI's hardware team) detailed how **AI wrote the Jalapeño MLA kernel** shown at Hot Chips. Plain-language: a normal compiler improves code by fixed local rules/heuristics; an **LLM acts as a "stochastic optimizer"** — it proposes optimizations like an expert human performance engineer, unconstrained by a rule set, taking many shots on goal. Lineage runs to the **2013 STOKE paper** (randomly mutate a program searching for the optimum) with LLM reasoning swapping in for the random walk. The AI takes the compiler's **"emitter"** role — lowering a numpy-level spec to optimized code — and because outputs are **verified for semantic equivalence** against the spec, nobody reads the kernels (like the assembly `C++ -O3` emits). "Start near numpy, wait 48 hours, out comes a kernel" often beating hand-tuned expert code. Why it matters for the theme: this is the mechanism behind the ~9–16-month "hiring-to-tapeout" cycles making labs (OpenAI/Anthropic) viable chip designers — a *demand* pull for verification/EDA, not a replacement. Ties to [[custom-silicon-asic]].
