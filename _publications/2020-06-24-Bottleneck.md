---
title: "Is Network the Bottleneck of Distributed Training?"
collection: publications
permalink: /publication/2020-06-24-Bottleneck
excerpt: 'This paper is about distributed training of DNN models.'
date: 2020-06-24
venue: 'NetAI 2020'
paperurl: 'https://arxiv.org/pdf/2006.10103'
# citation: 'Your Name, You. (2010). &quot;Paper Title Number 2.&quot; <i>Journal 1</i>. 1(2).'
---

Recently there has been a surge of research on improving the communication efficiency of distributed training. However, little work has been done to systematically understand whether the network is the bottleneck and to what extent.
In this paper, we take a first-principles approach to measure and analyze the network performance of distributed training. As expected, our measurement confirms that communication is the component that blocks distributed training from linear scale-out. However, contrary to the common belief, we find that the network is running at low utilization and that if the network can be fully utilized, distributed training can achieve a scaling factor of close to one. Moreover, while many recent proposals on gradient compression advocate over 100x compression ratio, we show that under full network utilization, there is no need for gradient compression in 100 Gbps network. On the other hand, a lower speed network like 10 Gbps requires only 2x-5x gradients compression ratio to achieve almost linear scale-out. Compared to application-level techniques like gradient compression, network-level optimizations do not require changes to applications and do not hurt the performance of trained models. As such, we advocate that the real challenge of distributed training is for the network community to develop high-performance network transport to fully utilize the network capacity and achieve linear scale-out.

[Paper](https://arxiv.org/pdf/2006.10103), [Code](https://github.com/netx-repo/training-bottleneck)

<!-- Recommended citation: Your Name, You. (2010). "Paper Title Number 2." <i>Journal 1</i>. 1(2). -->