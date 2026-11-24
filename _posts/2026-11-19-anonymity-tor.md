---
layout: post
title: "Don’t get caught, keep your Onions in a Vault"
date: 2026-11-17
paper_authors: "H. Ikram, R. Habib, M. Ali, Z. A. Uzmi"
paper_venue: "NINeS 2026"
paper_url: "https://doi.org/10.4230/OASIcs.NINeS.2026.17"
week: 9
tags: [tor, anonymity, hidden-services, trusted-execution-environments]
---

## Key Idea
The authors propose a novel method for protecting Tor hidden-services (HS) from deanonymization attacks by offloading them to an incentivized third-party "vault" running a Trusted Execution Environment (TEE).

## Critique
The main issue with this implementation is the reliance on a trusted execution environment (TEE), especially since the authors exclude side-channel attacks from their threat model. These devices can be exploited via side-channel attacks by a malicious vault owner with physical access, which removes the confidentiality and integrity guarantees the vault provides. Additionally, it is risky to hand over your hosted application to an untrusted third party. While the original provider's IP is safer, the worst-case scenario for the vault operator is still deanonymization (since they must stay online continuously), and for the provider, it is having their private keys or data stolen.

## Connections
This work is unique as it covers TOR networks.
