---
layout: post
title: "Simulate Before Sending: Rethinking Transport in Datacenter Networks"
date: 2026-10-05
paper_authors: "D. Straussman, I. Keslassy, A. Shpiner, L. Liss"
paper_venue: "NINeS 2026"
paper_url: "https://doi.org/10.4230/OASICS.NINES.2026.19"
week: 5
tags: [datacenter-networks, transport-protocols, ai-training, lossless-networks]
---
## Key Idea
The authors propose dcSim, an efficient transport that achieves lower CCTs and practically lossless performance in commodity datacenter networks. The main idea is to \"simulate before sending\", where each packet first employs a small simulation probe to explore congestion along a candidate path. Only packets whose simulation probes succeed are then transmitted. The evaluations confirm that dcSim achieves faster CCTs than existing schemes with small queues and virtually zero packet loss.

## Critique
The main contribution of this work is the proactive approach to avoiding packet loss and retransmissions which significantly degrade performance in AI training. A potential limitation is the potential overhead of simulation probes. 

## Connections
The dcSim approach is similar to the work in the congestion control paper (McClure et al.), as both focus on optimizations for modern datacenter networks. While the congestion control paper suggests that many INT signals do not significantly improve performance, dcSim takes a different approach by proactively simulating paths. Furthermore, while P-ECMP focuses on routing and path control, dcSim focuses on the transport layer to resolve network anomologies.
