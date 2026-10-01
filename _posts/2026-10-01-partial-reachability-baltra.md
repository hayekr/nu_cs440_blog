---
layout: post
title: "Understanding Partial Reachability in the Internet Core"
date: 2026-10-01
paper_authors: "G. Baltra, T. Saluja, Y. Pradkin, J. Heidemann"
paper_venue: "NINeS 2026"
paper_url: "https://doi.org/10.4230/OASIcs.NINeS.2026.4"
week: 2
tags: [internet, internet-reliability, network-outages, active-measurements]
---

## Key Idea

The goal of the internet is to allow separate networks to communicate in a decentralized manner, i.e, universal reachability. Today, it is observed that due to various pressures, the internet only has partial reachability. The authors propose that this partial reachability is fundamental to the internet. They claim the internet contains two kinds of persistent unreachability: peninsulas and islands. They develop a strong measurement methodology, propose detection algorithms, and quantify the existence of these unreachable entities. The main finding of their measurement campaign is that peninsulas, i.e., persistent unreachability, are more common than Internet outages.


## Critique

The paper is very well written. The research question is clearly motivated, and all necessary components are thoroughly defined. As thorough as the authors are, I think a clear overview of the *Trinocular*, *RIPE Atlas*, and *Ark* datasets could be placed in the introduction. 
Additionally, this study's databases are constrained on the location of the Vantage Points (VPs). Though the authors do cross-validate their results against *Ark*, additional vantage points, particularly within networks identified as peninsulas or islands, could provide another perspective on the results. Lastly, the use of ICMP in the Trinocular dataset raises a concern on what *reachability* means in this study. ICMP responses are able to sufficiently determine the internet-layer connectivity; however, they do not adequately characterize the reachability of application-level services that users of ASes find important.



## Connections
I do not find that this paper relates to the invariants defined in "What Can We Actually Rely On About the Internet?". However, it can be said that two articles share a methodological concern: the same underlying assumution of using VP's that one does not control could influence the measurement results.