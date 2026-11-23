---
layout: post
title: "BISCAY: Practical Radio KPI Driven Congestion Control for Mobile Networks"
date: 2026-11-17
paper_authors: "J. Larrea, T. Shreedhar, A. Niemi, A. Sefiane, M. K. Marina"
paper_venue: "NINeS 2026"
paper_url: "https://doi.org/10.4230/OASIcs.NINeS.2026.15"
week: 8
tags: [cellular-networks, congestion-control, lte, 5g]
---

## Key Idea
BISCAY is a radio key-performance indicator (KPI)-based congestion control algorithms (CCA) that infers cellular bandwidth via OpenDiag. BISCAY extracts KPIs from the UE's radio chipset to derive cellular link bandwidth. Modern CCAs are not able to properly estimate bandwidth and latency dynamics in cellular networks because congestion may be due to poor channel quality. Thus, BISCAY implements OpenDiag to derive radio link bandwidth from the MAC layer, with an update time ~100ms. The authors demonstrate that BISCAY achieves the highest throughput and lossless delays on mobile while also decreasing the tail delay with two and three simultaneous flows.

## Critique
OpenDiag is tied directly to Qualcomm UEs. While the authors acknowledge that most devices are based on Qualcomm modems, modifications of the Diag system can poorly affect this protocol and break KPI extraction. A more fundamental critique is that the information provided to the CCA is also available at the gNB. BISCAY reverse-engineers Diag and hooks into a potentially dynamic system to extract TBS and PRBs; however, this information is natively available at the gNB. A congestion control algorithm that the carrier implements at their gNB that takes CQI into account may be more feasible.

## Connections
This relates to LeoCC and Viadaptive, as it is also a CCA that determines congestion control based on more accurate channel estimation.
