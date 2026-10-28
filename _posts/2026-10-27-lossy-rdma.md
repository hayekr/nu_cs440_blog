---
layout: post
title: "Revisiting RDMA Reliability for Lossy Fabrics"
date: 2026-10-27
paper_authors: "W. Li, X. Liu, Y. Zhang, Z. Wang, W. Gu, T. Qian, G. Zeng, S. Ren, X. Huang, Z. Ren, B. Liu, J. Zhang"
paper_venue: "SIGCOMM 2025"
paper_url: "https://doi.org/10.1145/3718952.3750480"
week: 5
tags: [rdma-nics, reliability, lossy-fabrics, lossless-control-plane]
---

## Key Idea
The authors introduce an RDMA transport architecture called DCP that is designed around: independence of PFC, packet level load balancing, fast retransmisison, and hardware implementation. DCP separtes the contorl and data plane, ensuring a lossless control plane and lossy dataplane. To accomplish lossless control and fast retry, DCP implements header-only retransmission, where the network swtich trims packet data given load balancing requirements. This header-only packet is then forwarded back to the sender for retransmission. This control flow mitigates blocking issues that PFC causes. Further, DCP eliminates reorder buffers and tracking bitmaps by extending headers for direct OOO memory placement.

## Critique
The paper is well written and provides measningful improvement over existing protocols. However, the evaluation reveals that DCP struggles under heavy incast without active congestion control. Additionally, it would be beneficial to examine the cost of DCP's timeout fallback. Tiemouts are eliminated during normal operation due to HO retry; however, in the the event that HO packets are dropped, this breaks the system assumptions, forcing timout-based retry.
## Connections
This paper connects to ECMP programmability for flow control and DC-TCP for differnet implementaions of lossless flow control.
