---
layout: post
title: "DistTrain: Addressing Model and Data Heterogeneity with Disaggregated Training for Multimodal Large Language Models"
date: 2026-10-29
paper_authors: "Z. Zhang, Y. Zhong, Y. Jiang, H. Hu, J. Sun, Z. Ge, Y. Zhu, D. Jiang, X. Jin"
paper_venue: "SIGCOMM 25"
paper_url: "https://doi.org/10.1145/3718958.3750472"
week: 6
tags: [large-language-models, multimodal-models, distributed-training]
---

## Key Idea
The authors present DistTrain, a disaggregated system for multimodal LLM training. The two main contributions of the framework is an orchestration system and a data preprocessing pipeline. Both of these systems allow LLM training compute clusters to achive higher FLOP utilization, outperforming the SOTA training framework.

## Critique
The author claim is that their framework is compatible with alternate modalities, however their evlauation only includes vision models. Additionally, it can be seen in the evaluation, the DistTrain framework does not outperform the Megatron-LM framework in the 72B parameter regime at the same scale as the smaller models. It would be beneficial to see evaluation on how DistTrain scales as the paramter count increases. Finally, a significant gap of this evaluation is a lack of convergence and loss curves; they simply add to the argument that the training framework produces better results

## Connections
I do not think there are backconnections here to prior networking papers. However, this work connects well to federated learning research on straggler reduction. Specifically, there is a large body of work pertaining to the minimization of the straggler effect to allow for more efficient training.
