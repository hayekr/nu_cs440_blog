---
layout: post
title: "No Signal to Rule Them All: A Systematic Analysis of In-Network Congestion Signals"
date: 2026-10-15
paper_authors: "S. McClure, N. Dukkipati, S. Ratnasamy, S. Shenker"
paper_venue: "NINeS 2026"
paper_url: "https://drops.dagstuhl.de/storage/01oasics/oasics-vol139-nines2026/OASIcs.NINeS.2026.12/OASIcs.NINeS.2026.12.pdf"
week: 4
tags: [congestion-control, in-network-telemetry]
---

## Key Idea
Congestion Control Algorithms (CCA) have evolved significantly since the introduction of the internet, and are becoming highly imporant due to the prevalence of datacenters. In-network telemetry (INT) is internal signals at the network devices that are used to assist datacenter centric CCAs. The authors generalize the use of INTs for CCAs and aim to explore what INT signals are most valuable for a datacenter CCA. Learned CCAs are proposed as a way to optimize CCAs for INT signals; however, the authors assert that these algorithms are not sutiable for large-scale deployment because of their lack of generalization. The main finding is that INT signals, regardless of what is signaled, does not significantly improve the performance of CCAs, compared to simply using end-to-end signaling.

## Critique
The main limitation in the methodology of this work is the reliance on *lCCA*. The paper acknowledges that analytically optimal CCA's are intractable, and instead utilize R+ to produce CCA's. Consequently, the results from the R+ simulation are not necessarily realistic, and will overreflect the specific training conditions. Additionally, the number of INTs used in the simulation is minimal, and may not generalize to all INTs.


## Connections
