---
type: source
title: "2025 AI Diffusion Export Controls - Microsoft Regulatory Capture, Oracle Tears, Impacts Quantified, Model Restrictions"
tags: []
related: []
created: 2025-01-15
updated: 2025-01-15
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/2025-ai-diffusion-export-controls-microsoft-regulatory-capture-oracle-tears"
venue: SemiAnalysis
post_date: 2025-01-15
tickers: [MSFT, GOOGL, AMZN, ORCL, NVDA]
---
[[semianalysis]] dissects the US Bureau of Industry and Security's January 13, 2025 Framework for Artificial Intelligence Diffusion — the most sweeping AI export control regime ever enacted — arguing it constitutes effective regulatory capture by Microsoft, Amazon, and Google while severely constraining competitors like Oracle and curtailing Nvidia's addressable market.

**The three-tier framework.** The rule divides the world into Tier 1 (US plus 18 allies: Japan, South Korea, UK, Germany, etc.), Tier 3 (23 arms-embargoed nations plus Macau, effectively a ban), and Tier 2 (all others: Malaysia, India, Singapore, UAE, Brazil). Each Tier 2 country receives a hard cap of ~49,901 H100-equivalent GPUs installable through 2027 (doubling to ~99,802 with a government alignment agreement). The author notes that a single 20,000-GPU GB200 cluster from one cloud company can consume an entire country's allocation.

**Validated End User (VEU) structure favors hyperscalers.** Universal VEUs (UVEUs) — primarily Microsoft, Google, Amazon, and Meta — must keep 75% of controlled compute in Tier 1 countries and no more than 7% in any single Tier 2 nation; US-headquartered UVEUs face a 50% domestic compute floor. This structure is custom-fitted to the existing footprint of US hyperscalers, leading the author to characterize the rule as "unabashedly nationalistic" and an act of regulatory capture. National VEUs (NVEUs) for Tier 1/2 companies receive narrower, destination-specific authorizations capped at roughly 320,000 H100 equivalents.

**Oracle singled out as the primary loser.** Oracle's overseas-heavy deployment model conflicts directly with the UVEU residency requirements. The analysis describes Oracle as "severely limited" and its existing international cloud buildout as effectively non-compliant under the new framework — a structural impediment competitors headquartered domestically do not face.

**Nvidia: reduced TAM, lower-margin products.** China remains Tier 3, confining Nvidia to lower-performance, lower-margin H20/B20 derivatives for that market. Broader Tier 2 caps suppress total GPU deployment internationally, compressing the incremental opportunity outside the US and Tier 1 allies.

**Frontier model controls.** Models requiring ≥1×10²⁶ training FLOPs (roughly 2× Llama 405B) may only be trained in Tier 1 countries. Fine-tuning elsewhere is capped at 25% of original operations or 2×10²⁵ FLOPs. Closed-weight models at or above this threshold face export licensing with a "presumption of denial." Open-source models and any model smaller than the largest publicly released open-source model are exempt.

**Enforcement skepticism.** The author flags the LPP (Low Processing Performance) exemption — ~1,699 H100-equivalents per customer per year with notification only — as a circumvention vector replicating Huawei's historical IC procurement playbook via shell entities. Counting training FLOPs for synthetically generated data is dismissed as "technically challenging at best and infeasible at worst."

**Geographic winners and losers.** US domestic datacenter capacity (10+ gigawatt-scale campuses within two years) benefits from onshoring incentives. Malaysia's 3 GW of datacenter pipeline faces severe quota constraints. Brazil and the Middle East are comparatively better positioned within Tier 2 due to large planned capacity and improved regulatory treatment, respectively.

## Calls

- [[MSFT]] — LONG — px@n/a — UVEU structure mirrors Microsoft's existing footprint; regulatory capture positions Microsoft to dominate global AI cloud infrastructure buildout.
- [[GOOGL]] — LONG — px@n/a — Co-beneficiary of UVEU framework alongside Microsoft; domestic compute concentration aligns with existing Google Cloud architecture.
- [[AMZN]] — LONG — px@n/a — AWS qualifies as a UVEU beneficiary; domestic-first deployment model fits the 50% US compute floor with minimal restructuring.
- [[ORCL]] — SHORT — px@n/a — Oracle's overseas-heavy cloud strategy is structurally incompatible with UVEU residency requirements, constraining international expansion.
- [[NVDA]] — NEUTRAL — px@n/a — China locked out (Tier 3) and Tier 2 caps reduce total addressable GPU deployments; company steered toward lower-margin H20/B20 export variants.
