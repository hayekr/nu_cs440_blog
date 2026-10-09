---
layout: post
title: "Unlocking ECMP Programmability for Precise Traffic Control"
date: 2026-10-08
paper_authors: "Y. Liu, Y. Xiao, X. Zhang, W. Dang, H. Liu, Z. Li, Z. He"
paper_venue: "NSDI2025"
paper_url: "https://www.usenix.org/system/files/nsdi25-liu-yadong.pdf"
week: 3
tags: [network-properties, traffic-engineering, performance-analysis]
---

## Key Idea
ECMP is the industry standard method to route traffic within data center networks. The main limitation is that for scenarios to manage network anomologies wiht precise network control (PTC). By leveraging ECMP groups, operators can achieve precise path control. The authors evaluate P-ECMP on both a real world deployment and a large-scale simulation. 

## Critique
The P-ECMP paper is well written and proposes a meaningful addition to an industry standard application by taking advantage of pre-existing features. However, the main evaluation being simulation based on NS3 is a limitation. Additionally, evaluation of the control protocol more topologies, in additon to trees would be an interesting addition.

## Connections
The P-ECMP protocol can be particularly useful in optimizing against downtime in datacenters. Although this is similar to partial reachability of the internet, there is difference in the causes of downtime between partial reachability and the purpose of P-ECMP. Conversely, the RAHA protocol could be used in conjunction with P-ECMP, to precisely control a large scale network to resolve unforseen failures.