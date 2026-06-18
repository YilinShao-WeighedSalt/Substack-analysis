---
type: source
title: "Datacenter Anatomy Part 1: Electrical Systems"
tags: []
related: []
created: 2024-10-14
updated: 2024-10-14
authors: [semianalysis]
year: 2024
url: "https://newsletter.semianalysis.com/p/datacenter-anatomy-part-1-electrical"
venue: SemiAnalysis
post_date: 2024-10-14
tickers: [NVDA, VRT]
---

[[semianalysis]] provides a detailed technical taxonomy of datacenter electrical infrastructure, framing the supply chain and design consequences of AI-driven power density escalation — from utility transformers down to rack-level power distribution.

## Power Density Inflection

The central thesis is that AI infrastructure has shattered legacy power-density assumptions. Traditional datacenters operated below 10 kW per rack; Nvidia's GB200 NVL72 systems require 130 kW+ per rack — a roughly 13x increase. This has forced hyperscalers to redesign facilities from the ground up, and is causing cascading supply chain stress across the entire electrical stack.

## Facility Classification

The post maps Uptime Institute Tier ratings (1–4) to real hyperscaler deployment patterns. Tier 3 facilities require "concurrent maintainability" with N+1 redundancy on transformers and generators, and 2N redundancy on power distribution. Most hyperscale campuses are built to Tier 3 or a customized equivalent, balancing redundancy cost against availability targets.

## Electrical Power Path

The full power path runs: utility high-voltage grid → campus substation (50–100 MVA transformers) → medium-voltage switchgear (11–33 kV distribution) → pod-level step-down transformers → low-voltage distribution → UPS systems → PDUs/busways → IT equipment. Each stage introduces conversion losses that compound to affect overall PUE.

## Transformer Bottleneck

High-voltage transformers are identified as a critical supply chain chokepoint. Lead times exceed 12 months, driven by a shortage of Grain Oriented Electrical Steel (GOES) — a niche material with a limited global supplier base. Hyperscalers are increasingly pre-ordering transformers years in advance to secure capacity.

## Redundancy Schemes

Advanced hyperscaler designs employ schemes such as 4N3R (four systems available, three required for full load) and "Catcher" configurations using Static Transfer Switches, which provide sub-cycle failover — far faster than mechanical Automatic Transfer Switches. Diesel generators (2–3 MW per unit) remain the standard backup, with a 300 MW campus requiring dozens of units on standby.

## Meta vs. Google Design Comparison

Meta's "H" building design requires up to 36 generators per structure and takes approximately two years to construct. Google's facilities use 34 larger generators in buildings that are roughly half the footprint, achieving over 3x greater power density per square foot relative to Meta. This design advantage is not merely aesthetic — it translates directly into faster deployment of AI training capacity.

## Key Suppliers

Primary electrical infrastructure vendors serving hyperscalers include Vertiv (VRT), Schneider Electric, Eaton, Legrand, and Delta. The post tracks 200+ datacenter suppliers with SKU-level demand forecasting through 2030.

## Scale Context

A 300 MW datacenter campus consumes electricity equivalent to approximately 200,000 US households annually. A 20,840-H100 cluster requires roughly 25.9 MW of critical IT power capacity.

## Calls

- [[NVDA]] — MENTION — px@n/a — GB200 NVL72's 130 kW+ rack power requirement is the primary forcing function driving the entire electrical infrastructure redesign wave described in this report
- [[VRT]] — MENTION — px@n/a — Vertiv cited as a primary supplier of datacenter electrical infrastructure components positioned to benefit from AI-driven power density escalation
