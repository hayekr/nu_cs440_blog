---
layout: post
title: "GREEN: Carbon-efficient Resource Scheduling for Machine Learning Clusters"
date: 2026-10-29
paper_authors: "K. Xu, D. Sun, H. Tian, J. Zhang, K. Chen"
paper_venue: "NDSI 25"
paper_url: "https://www.usenix.org/conference/nsdi25/presentation/xu-kaiqiang"
week: 6
tags: [sustainable-computing, efficient-scheduling]
---

## Key Idea
The authors introduce an carbon-aware resource schedule for machine learning training workloads called GREEN. The GREEN framework centers around two optimizers: the energy efficient and carbon footprint optimizer. They evaluate their framework against five other similar resource schedulers using 791 collected real jobs from university production servers. They find that the GREEN framework results in roughly 41% reduction of carbon footprint at the expense of only 4% job completion time. Additionally, they evaluate the framework on a trace-based simulation workflow using indistry traces on 400 job submissions. In the simulation they find similar results. 

## Critique
The main critique of this work is the unrealistic real-world job scenarios. Modern architectures rely on distributed strategies, as described in [DistTrain](#2026-10-29-dist-train-ml.md). The strategy of incrementally adding single GPU's to a training run is infeasible. Second, the models evaluated are out-of-date. Image classification training workloads that last on the order of days are not representative of modern ultra-high parameter LLM workloads where training can scale on orders of weeks. Lastly, academic cluster workloads may not accuratly mimic the behbaviors of large scale ML workflows; however, this is addressed in their trace-based simulation evaluation.


## Connections
This work relates to the DistTrain protocol. The DistTrain protocol's goal is to optimize for resource utilization, while GREEN optmimzies for carbon intensity while minimially affecting job completion time. It would be interesting future work to see how temporal shifting with respect to carbon intensity curves affects the resource scheduling in DistTrain.
