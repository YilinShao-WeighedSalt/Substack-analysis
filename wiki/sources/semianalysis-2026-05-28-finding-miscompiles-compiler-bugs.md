---
type: source
title: "Finding Miscompiles for Fun, Not Profit"
tags: []
related: []
created: 2026-05-28
updated: 2026-05-28
authors: [semianalysis]
year: 2026
url: "https://newsletter.semianalysis.com/p/finding-miscompiles-for-fun-not-profit"
venue: SemiAnalysis
post_date: 2026-05-28
tickers: []
---

Justin Lebar, a compiler veteran with stints at Google, Waymo, and OpenAI, documents a week-long experiment in which AI agents — not human engineers — drove a compiler bug-finding campaign that cost over $10,000 but uncovered hundreds of plausible bugs across multiple backends. Published on [[semianalysis]].

## Fuzzing LLVM instcombine (January 2026)

Lebar's first experiment used Codex to co-develop a fuzzer targeting LLVM's instcombine optimization pass. Over several weeks the fuzzer found and fixed five bugs before the discovery rate dropped off. The LLM's key contribution was automating the tedious post-bug update of the fuzzer itself — an iterative loop that would have been laborious to run manually.

## Pivoting to NVIDIA ptxas (Mid-May 2026)

After joining SemiAnalysis, Lebar applied the same methodology to NVIDIA's closed-source ptxas compiler. Within three days he had 40 confirmed miscompiled programs; within a week the count was roughly 80. The model handled the repetitive work of mutating test cases between each find, dramatically compressing the human-hours required.

## LLVM AMDGPU Backend

The fuzzing technique was then extended to LLVM's AMDGPU backend at comparable bug-discovery rates. When personal ChatGPT Pro credits ran out, Lebar switched to Claude Opus 4.7 and reported no perceptible quality difference.

## Code Inspection Agents: The Inflection Point

The methodology changed materially when Lebar shifted from fuzzing to deploying 50 concurrent Claude subagents performing code inspection. Discovery rates jumped to one bug every four minutes on the LLVM codebase, and two per minute on the x86 backend — with no apparent saturation.

Bug quality differed by method: fuzzer-discovered bugs were all demonstrable miscompiles and generally higher severity; agent-discovered bugs averaged lower severity but caught classes of issues fuzzing cannot reach. The most alarming agent find: LLVM silently transforms an atomic store into two non-atomic stores — a data corruption vulnerability that could be catastrophic in production.

## Cost and Implications

Total spend: ~$1,000 for the fuzzer phase (several days, Opus 4.7); over $10,000 for the code inspection agent phase (a few hours). Lebar argues a single atomics bug in production easily exceeds $10,000 in damage, so the economics are favorable for well-resourced organizations. A June 1 update noted that Opus 4.8 plus "ultracode" mode cut cost-per-bug by ~80%, further improving the calculus.

The central thesis: "Things that were impossible five months ago are now 'just' Very Expensive." Token budgets now gate access to capabilities that simply did not exist before, creating an expanding gap between organizations that can and cannot afford large-scale AI-assisted security research.

## Calls

No ticker calls in this post.
