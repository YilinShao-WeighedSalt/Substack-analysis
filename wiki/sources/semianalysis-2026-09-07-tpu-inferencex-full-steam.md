---
type: source
title: "TPU Inference Externalization Full Steam Ahead — InferenceX"
tags: [tpu, ironwood, inference, torchtpu, custom-asic, google, nvidia]
related: ["[[semianalysis]]", "[[GOOGL]]", "[[NVDA]]", "[[AMD]]", "[[custom-silicon-asic]]", "[[ai-accelerator-competition]]", "[[nvidia-gpu-platform]]"]
created: 2026-09-08
updated: 2026-09-08
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/tpu-inferencex-full-steam"
venue: SemiAnalysis
post_date: 2026-09-07
tickers: [GOOGL, NVDA, AMD]
---

# TPU Inference Externalization Full Steam Ahead — InferenceX

The marquee datapoint: **the first third-party inference benchmarks for TPUv7 Ironwood**,
run on SemiAnalysis's InferenceX harness against Nvidia B200/B300. The question that has
hung over TPUs for a decade — *can an outside buyer beat Nvidia on the economics that
matter?* — gets its first public answer.

## Key arguments

- **Ironwood delivers up to ~50% better performance-per-dollar than B200/B300** on
  FP8 aggregated serving (Qwen3.5-397B), across much of the Pareto curve, on both
  Google-internal TCO ($1.03/chip-hr) and external-buyer TCO. At 20 tok/s/user it even
  leads on **raw throughput** (9,364 vs ~8,900 tok/s/chip) → +50% tok/$ vs B200,
  +96% vs B300. TPU's lower hourly cost offsets lower raw throughput.
- **The catch**: TPUv7 has **no native FP4** — on FP4, Nvidia still leads (FP4-vs-FP8
  isn't apples-to-apples on quality). **TPUv8i** adds native FP4 → SemiAnalysis expects
  **Boardfly to be competitive with Rubin NVL72.** Also, external disagg serving isn't
  optimized yet, so GB300 NVL72 disagg still wins the mid-latency band by ~30% today
  (expected to close in months).
- **TorchTPU** — the new native-PyTorch backend (replaces the TorchAX→JAX translation
  layer) — lets vLLM/SGLang treat TPUs as first-class `device="tpu"` PyTorch devices.
  In **private beta now, open-sources ~mid-October** at the PyTorch Conference. This is
  the software bridge that makes TPUs usable outside Google.
- SemiAnalysis's verdict: **unlike AMD** (still "learning to build a test-first software
  culture"), Google has decades of quality-driven software engineering, so external TPU
  software should mature *rapidly*. **Anthropic is the biggest TPU user** (>1M committed:
  ~400k purchased + 600k rented via GCP), surpassing DeepMind's own use by 2029.
- Deep technical sections: DP-attention/EP kernels, MoE routing on SparseCore, GDN
  kernel fusion, the 256×256 MXU tile-geometry tax ("TPUs are picky" about head dims),
  the 3D-torus/OCS scale-out, and TPUv8i's Boardfly high-radix fabric (16→7 hops,
  19.2 Tb/s ICI, 384 MB SRAM for on-chip KV cache).

## Calls

- **LONG [[GOOGL]]** $338.46 — TPU externalization is real and moving fast; first 3rd-party proof of ~50% better perf/$ on inference; TorchTPU open-sources in October, turning TPU into a merchant AI-silicon product.
- **NEUTRAL [[NVDA]]** $230.36 — TPUv7 pressures Blackwell inference economics, but no native FP4 means Rubin/FP4 still leads; TPUv8i is the real contest.
- **NEUTRAL [[AMD]]** $477.57 — explicitly dinged: still learning a test-first software culture, unlike Google's mature quality culture — software, not silicon, is AMD's gap.
