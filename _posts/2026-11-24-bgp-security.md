---
layout: post
title: "Passive Data-Plane Telemetry to Mitigate Long-Distance BGP Hijacks"
date: 2026-11-17
paper_authors: "S. Sengupta, H. Kim, D. Jubas, M. Apostolaki, J. Rexford"
paper_venue: "NINeS 2026"
paper_url: "https://doi.org/10.4230/OASIcs.NINeS.2026.14"
week: 9
tags: [network-security, routing, border-gateway-protocol, hijack, interception, attack, programmable-networks, in-network-detection, in-network-mitigation]
---

## Key Idea
BGP hijacks are a critical vulnerability of traffic routed between autonomous systems (AS). The authors consider an RTT-based passive BGP hijack detection system that lies at the dataplane. During a BGP hijack, there is expected to be a significant increase in RTT as a result of the attack. This is justified by an evaluation of the minimum and maximum inter- and intra-country distances. They find that most countries are able to detect attacks via only RTT monitoring. The system HiDe monitors data plane packets and matches acks to drive an RTT. When an RTT spikes unexpectedly, it is triggered as an alert attack is in progress.

## Critique
The paper proposes BGP attacks from nation states. Sufficiently determined states can circumvent this detection by placing their attack vector within country borders or within a distance such that the detection software does not see a significant increase in RTT. 

## Connections
This work relates to the discussed paper about BGP routing stability and additionally to the security point of view in the Tor paper.
