---
type: source
title: "How AI Labs Are Solving the Power Crisis: The Onsite Gas Deep Dive"
tags: []
related: []
created: 2025-12-30
updated: 2025-12-30
authors: [semianalysis]
year: 2025
url: "https://newsletter.semianalysis.com/p/how-ai-labs-are-solving-the-power"
venue: SemiAnalysis
post_date: 2025-12-30
tickers: [GEV, SMNEY, BE, CAT, HWM, CMI]
---
[[semianalysis]] argues that the electrical grid has become the binding constraint on AI infrastructure buildout, and that hyperscalers and AI labs are solving it by deploying "Bring Your Own Generation" (BYOG) onsite power — bypassing utility interconnection queues entirely. Getting a 400 MW datacenter online six months faster is worth billions given AI revenue yields of $10–12 billion per gigawatt annually, which makes expensive onsite generation economically rational even at a premium to grid rates.

**Why the grid fails AI.** Texas receives tens of gigawatts of datacenter load requests monthly yet approves less than 1 GW annually. Real-time balancing requirements and multi-year system studies are structurally incompatible with AI's deployment timelines. xAI exploited state-border permitting arbitrage, submitting permits across the Tennessee/Mississippi border and ultimately building in Mississippi when Tennessee could not meet timelines.

**Technology landscape.** Four generation technologies compete: (1) Aeroderivative gas turbines (GE Vernova LM2500/LM6000, Mitsubishi FT8) at $1,700–2,000/kW capex with 5–10 minute ramp times; (2) industrial gas turbines including heavy-duty H-class units (GE Vernova, Siemens Energy, Mitsubishi, newcomer Doosan Enerbility) capable of 200+ MW per unit; (3) reciprocating engines (RICE) from Wärtsilä, Cummins, and Caterpillar's Jenbacher brand at similar capex but better partial-load efficiency; and (4) Bloom Energy solid-oxide fuel cells at $3,000–4,000/kW — a premium justified by no-combustion permitting advantages and short installation timelines (weeks vs. 18–36 months for turbines).

**Real deployments.** xAI deployed 500 MW+ using truck-mounted Solar Turbines (Caterpillar subsidiary, 16 MW each) within months by renting equipment to sidestep lead times and paired them with Tesla Megapacks for sub-second inertia buffering. Vantage DC is building a 1.4 GW campus in Shackelford County, TX with 2.3 GW of VoltaGrid systems (64% overbuild for N+1 redundancy). Crusoe/OpenAI's Abilene site uses 5x GE LM2500XPRESS plus 5x Titan 350 turbines (~360 MW). Meta/Williams' Socrates South project deploys a mixed fleet totaling 306 MW nameplate.

**Supply chain bottlenecks.** Turbine core castings are produced by only four Western firms: Precision Castparts (private, Berkshire subsidiary), Howmet Aerospace, Consolidated Precision Products, and Doncasters. All face constraints in rare earth inputs — rhenium, yttrium, cobalt, tantalum, tungsten — several of which are under Chinese export controls. GE Vernova guides to 24 GW/year capacity with no factory expansion; Siemens Energy targets >30 GW by 2028–2030. Manufacturers are deliberately cautious due to institutional memory of catastrophic overcapacity after the 2001 deregulation bubble when GE shipped 60 GW in a single year and demand then collapsed below 10 GW/year from 2017–2022.

**New entrants.** Boom Supersonic's "Superpower" aeroderivative (42 MW/unit at high ambient temps, ~$1,000/kW hardware) has booked 1.2 GW with Crusoe. ProEnergy retrofits Boeing 747 CF6-80C2 jet engines into aeroderivatives. Doosan Enerbility's DGT6 H-class turbine has already secured 1.9 GW of orders from xAI, a rare new-entrant success in a decade-old oligopoly.

## Calls

- [[GEV]] — LONG — n/a — dominant aeroderivative and H-class turbine supplier capturing the largest share of the BYOG buildout; stock already surging but supply constraints limit downside risk to demand disappointment
- [[SMNEY]] — LONG — n/a — Siemens Energy among the clear winners in onsite gas turbine demand; targeting >30 GW/year capacity by 2028–2030 with explicit datacenter order momentum
- [[BE]] — LONG — n/a — Bloom Energy fuel cells command $3,000–4,000/kW premium justified by permitting speed advantages; targeting 2 GW/year production by end of 2026
- [[CAT]] — LONG — n/a — Caterpillar's Solar Turbines brand is the go-to for rapid truck-mounted deployments (xAI use case); company guiding to 2x engine and 2.5x turbine production by 2030
- [[HWM]] — MENTION — n/a — Howmet Aerospace is one of only four Western producers of turbine blade castings, a critical supply bottleneck that benefits incumbent precision casting firms
- [[CMI]] — MENTION — n/a — Cummins named as a RICE manufacturer competing in the onsite datacenter power market alongside Wärtsilä and Caterpillar's Jenbacher brand
