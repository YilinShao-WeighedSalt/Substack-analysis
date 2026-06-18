---
type: ticker
title: "SITM — SiTime"
tags: []
related: ["[[irrationalanalysis-2024-12-02-communication-systems-guide]]", "[[irrationalanalysis-2025-02-07-1qcy25-earnings-roundup]]", "[[irrationalanalysis-2025-02-16-optical-illusions-fn-cien-sitm-lite]]", "[[irrationalanalysis-2025-03-03-iphone-16e-sitm-qcom-out]]", "[[irrationalanalysis-2025-03-05-panther-lake-delay]]", "[[irrationalanalysis-2025-05-02-apple-modem-timeline]]", "[[irrationalanalysis-2025-08-01-august-1st-portfolio-update]]", "[[irrationalanalysis-2025-08-22-tower-semi-fabrinet-nvidia-1-6t]]", "[[irrationalanalysis-2025-09-18-qualcomm-is-out-of-time]]", "[[irrationalanalysis-2025-11-28-tpu-vs-nvda-avgo-intel-foundry]]", "[[irrationalanalysis-2025-12-21-2026-irrational-ideas]]", "[[irrationalanalysis-2026-01-01-2025-end-of-year-portfolio-update]]", "[[irrationalanalysis-2026-01-31-january-is-finally-over]]", "[[irrationalanalysis-2026-02-06-earnings-roundup-lite-cohr-sitm-qcom]]", "[[irrationalanalysis-2026-05-08-earnings-roundup-semis-optics]]"]
created: 2024-12-02
updated: 2026-05-08
ticker: SITM
current_stance: long
conviction: high
last_review: 2026-05-08
---
## Call log
| date | publication | stance | px@call | thesis |
|------|-------------|--------|---------|--------|
| 2024-12-02 | [[irrationalanalysis]] | LONG | n/a | Nvidia GB200 uses SiTime for programmable PPM cancellation; overlooked datacentre opportunity |
| 2025-02-07 | [[irrationalanalysis]] | LONG | n/a | Solid results; post-earnings selloff attributed to pod-fund overreaction; author aggressively bought dip |
| 2025-02-16 | [[irrationalanalysis]] | LONG | n/a | Programmable 0-PPM frequency sync is an unrecognized alpha opportunity validated by Nvidia GB200 design win; huge AI datacenter TAM |
| 2025-03-03 | [[irrationalanalysis]] | LONG | n/a | 70% probability MEMS oscillator returned to iPhone 16e connectivity board, replacing Quartz timer |
| 2025-03-05 | [[irrationalanalysis]] | LONG | n/a | Confirmed iPhone oscillator content; clock-forwarding advantage extends to datacenter SerDes |
| 2025-05-02 | [[irrationalanalysis]] | LONG | n/a | Direct beneficiary of faster Apple modem ramp; author owns a position and wants more |
| 2025-08-01 | [[irrationalanalysis]] | LONG | n/a | Long in long-only accounts; consumer electronics and Apple pull-forward exposure clouds trading reentry |
| 2025-08-22 | [[irrationalanalysis]] | LONG | n/a | Mild positive; PPM clock sync is a natural fit for ring-based transceiver architectures |
| 2025-09-18 | [[irrationalanalysis]] | LONG | n/a | Very positive beneficiary of full Apple internal modem transition; author explicitly long |
| 2025-11-28 | [[irrationalanalysis]] | LONG | n/a | Re-entry pending wash-sale period expiry |
| 2025-12-21 | [[irrationalanalysis]] | LONG | n/a | New 80 fs jitter parts approaching quartz parity |
| 2026-01-01 | [[irrationalanalysis]] | MENTION | n/a | Sold in panic deleveraging alongside BE; plans to repurchase in January |
| 2026-01-31 | [[irrationalanalysis]] | LONG | n/a | Holds shares; will buy more on weakness; datacenter tailwind offsets iPhone Air risk |
| 2026-02-06 | [[irrationalanalysis]] | LONG | n/a | FracN PLL advantage positions SiTime to capture 200G LO demand as quartz struggles with higher frequencies |
| 2026-05-08 | [[irrationalanalysis]] | LONG | n/a | Quartz killer thesis complete; PPM sync + jitter fix drives major gross margin expansion |

## Thesis evolution
The bull case opened in December 2024 when [[irrationalanalysis]] identified that Nvidia's GB200 used SiTime's programmable oscillator not to save PCB space but to guarantee 0-PPM frequency sync across every NVLink lane — a CDR-system advantage that only SiTime can offer via I2C-commanded FracN PLLs. Through early 2025 the thesis gained a second leg: Apple returning SiTime to the iPhone connectivity board for the C1 modem, confirmed by CEO disclosure in March 2025, added a consumer volume vector on top of the datacenter TAM. The full Apple modem ramp into the iPhone 17 cycle and beyond was framed as a further multiplier. By late 2025 a third dimension emerged: SiTime's FracN PLL makes it the natural local-oscillator solution for 200G-per-lane transceivers and ring-modulator-based CPO systems where quartz cannot meet PPM requirements. The February 2026 Renesas distribution deal was read as adding fracN PLL engineering capacity to close the remaining jitter gap. By May 2026 the author declared the "quartz killer" thesis structurally complete: new parts had brought jitter from 130+ fs to ~60 fs, approaching high-quality quartz at ~35 fs, while the PPM sync advantage remains inimitable. No publication in this set expresses a bearish view; the only friction was a tactical deleveraging sale in early January 2026 (wash-sale driven) that the author described as a forced move rather than a thesis change.

## Outcome tracking
No px@call values exist across any entry, so outcome tracking rests on thesis trajectory. The three core predictions have all progressed toward confirmation: the Nvidia GB200 PPM-sync design win was established at the outset and never disputed; iPhone 16e oscillator content was confirmed by both teardown analysis and the SiTime CEO in March 2025; and the Apple full-modem ramp accelerated on schedule through 2025. The 80 fs jitter parts announced by December 2025 and the further improvement to ~60 fs by May 2026 represent direct product-level evidence that the jitter gap to quartz is closing. The live bull view would be falsified by: (1) quartz vendors closing the PPM-programmability gap at competitive cost, (2) Apple abandoning or significantly slowing the full C1 modem rollout, or (3) SiTime failing to win meaningful datacenter CPO/200G-transceiver sockets beyond Nvidia GB200.
