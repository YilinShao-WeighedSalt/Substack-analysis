---
type: source
title: "[Market Memo] Orange Man Attempted Chinese Transceiver Ban"
tags: [optical-transceivers, export-controls, silicon-photonics, InP]
related: ["[[irrationalanalysis]]", "[[AXTI]]", "[[LITE]]", "[[COHR]]", "[[AAOI]]", "[[FN]]", "[[TSEM]]", "[[CIEN]]", "[[NOK]]", "[[silicon-photonics-interconnects]]", "[[geopolitics-export-controls]]"]
created: 2026-08-06
updated: 2026-08-06
authors: [irrationalanalysis]
year: 2026
url: "https://irrationalanalysis.substack.com/p/market-memo-orange-man-attempted"
venue: Irrational Analysis
post_date: 2026-08-05
tickers: [AXTI, LITE, COHR, AAOI, FN, TSEM, CIEN, NOK]
---

# [Market Memo] Orange Man Attempted Chinese Transceiver Ban

Emergency memo on the **Reuters report (Aug 4, 2026)** that the Trump administration is drafting restrictions on new-model Chinese data-center optical transceivers, likely via the FCC's equipment-authorization / Covered List frameworks. No formal rule text yet; the definition of a "Chinese transceiver" (place of manufacture, incorporation, ownership, R&D location) is undefined.

## Key arguments

- **The "security risk" rationale is bogus.** A transceiver is just a PHY converting electrical↔optical; all data is encrypted at the host endpoint. It cannot sniff data or install malware — CMIS registers are a limited command map gated by a signed public/private-key auth system (OIF-CMIS-05.4 §9.9.2). Same false argument used against Huawei 5G RRHs. "Just admit you want to ban Chinese stuff for economic reasons."
- **Only new models affected** — everyone already has all 1.6T flavors qualified, so the real bite is at 3.2T, which is far off.
- **"More than a shell" evasion:** Innolight, Eoptolink, Accelink et al. run USA-registered entities with all footprint in SE Asia (Malaysia/Thailand/Vietnam); IP licensed in, production (active alignment, PCB/module assembly, burn-in) done outside mainland China. Easy to get transceivers that are legally "not Chinese."
- **China's real edge is active alignment** (six-axis, sub-micron): "order of magnitude better than the West," custom machines, higher yield/coupling/throughput. TFC, Inno, Accelink, Eopto "wipe the floor" with the West. Fabrinet is the best *non-Chinese* CM only because everyone else is "unusably dogshit."
- **EML→SiPho pivot:** a SiPho transceiver uses ~50% less InP than EML but more active-alignment content. Pivoting the design is trivial; alignment capacity/throughput is the true constraint.
- **MAD dynamic:** China can't block InP wafer exports and the US can't cut off transceiver imports. De-coupling takes 2–3 years with spicy volatility. Trump admin is prodding hyperscalers — who were *already* aggressively designing out Chinese transceivers.

## Calls

- **[[AXTI]] — LONG** ($68.61). "Most important stonk," going 2–4× in 12–18 mo on the InP squeeze; but sold out *today* tactically ("risk too high") — one bad China-retaliation headline = a 15–20% single-day drop. IQE rising on the news is "tourism" (where does IQE even buy its InP wafers?).
- **[[LITE]] — LONG** ($826.26). "Good for Lumentum whatever happens."
- **[[COHR]] — LONG** ($328.22). "Good for Coherent" — uses Tower SiPho PIC.
- **[[AAOI]] — LONG** ($128.56). "Fun degen play," better short-term risk/reward than AXTI; massive transceiver capacity expansion. Owned.
- **[[FN]] — LONG** ($522.22). Fabrinet wins the de-coupling — only viable non-Chinese optical CM.
- **[[TSEM]] — LONG** ($211.14). LITE/COHR/AAOI all use Tower for SiPho PIC; unique Openlight PDK for integrated InP-on-SiPho is very valuable as active-alignment efficiency becomes the bottleneck.
- **[[CIEN]] — NEUTRAL** ($408.83). Long-haul, unaffected by the ban; the sell-then-weak-bounce was "stupidity."
- **[[NOK]] — NEUTRAL** ($9.58). Same as Ciena — long-haul, outside the blast radius.
