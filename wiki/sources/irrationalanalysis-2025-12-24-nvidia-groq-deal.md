---
type: source
title: "Truly Irrational: Nvidia/Groq Deal"
tags: []
related: []
created: 2025-12-24
updated: 2025-12-24
authors: [irrationalanalysis]
year: 2025
url: "https://irrationalanalysis.substack.com/p/truly-irrational-nvidiagroq-deal"
venue: Irrational Analysis
post_date: 2025-12-24
tickers: [NVDA]
---

[[irrationalanalysis]] reacts with genuine bewilderment to a reported deal in which Nvidia pays Groq roughly $20 billion for a non-exclusive technology license while simultaneously hiring away Groq's key technical staff. The structure is notable: it is a licensing deal, not an acquisition, so it avoids the regulatory approval process that a full buyout would require — yet the practical outcome may be similar, since the people who built and understand the IP are leaving with Nvidia.

The author spends meaningful time explaining why Groq's architecture is so unusual and therefore why the deal is puzzling. Groq is not a TPU clone or a conventional ASIC. It runs a 144-wide VLIW (Very Long Instruction Word) datapath across everything — compute and memory management alike — and carries zero off-chip DRAM, relying exclusively on SRAM. This is architecturally extreme compared with Google's TPU, which uses an 8-wide VLIW only for control logic while running a conventional architecture for the actual compute and maintaining a normal memory hierarchy. The author has covered Groq's architecture in depth in a prior post ("Very Long Incoherent Writeup," February 2024).

The licensing angle raises a sharp practical question: if Groq's engineering talent is absorbed into Nvidia, who provides technical support and roadmap development for any other licensee of the Groq IP? The license is non-exclusive in name, but the knowledge base is effectively exclusive once the team departs.

The author contrasts this deal unfavorably with Nvidia's earlier acquisition of Enfabrica, which the author viewed as strategically coherent. The Groq deal, by contrast, is described as something the author simply cannot rationalize, acknowledging they must be missing something.

## Calls

- [[NVDA]] — NEUTRAL — px@n/a — Nvidia's $20B non-exclusive Groq IP license is strategically puzzling; author expresses confusion rather than a directional view on the stock
