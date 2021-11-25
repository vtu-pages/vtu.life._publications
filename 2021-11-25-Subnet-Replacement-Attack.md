---
title: "Towards Practical Deployment-Stage Backdoor Attack on Deep Neural Networks"
collection: publications
permalink: /publications/2021-11-25-Subnet-Replacement-Attack.html
excerpt: "We propose the first gray-box and physically realizable weights attack algorithm for backdoor injection, namely **subnet replacement attack (SRA)**.<br/><img style='padding-top: 10px; width: 100%' src='/images/sra_workflow.png'>"
date: 2021-11-25
venue: 'ArXiv Pre-print'
author: "Xiangyu Qi*, <b>Tinghao Xie*</b>, Ruizhe Pan, Jifeng Zhu, Yong Yang and Kai Bu"
share: False
# paperurl: 'not-added-yet'
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

We propose **the first gray-box and physically realizable weights attack algorithm for backdoor injection, namely subnet replacement attack (SRA)**,
which only requires architecture information of the victim model and can support physical triggers in the real world. Extensive experimental simulations and system-level real-world attack demonstrations are conducted.
Our results not only suggest the effectiveness and practicality of the proposed attack algorithm,
but also **reveal the practical risk of a novel type of computer virus that may widely spread and stealthily inject backdoor into DNN models in user devices**.
By our study, we call for more attention to the vulnerability of DNNs in the deployment stage.

> Our code is publicly available at [https://github.com/Unispac/Subnet-Replacement-Attack](https://github.com/Unispac/Subnet-Replacement-Attack).

<img style='padding-top: 10px; width: 100%' src='/images/sra_workflow.png'>

## Results

Attack results on CIFAR-10 models:

<img style='padding-top: 10px; width:60%' src='/images/sra_cifar10_bars.jpg'>


Attack results on ImageNet models:

<img style='padding-top: 10px; width:80%' src='/images/sra_imagenet_bars.jpg'>

Physical attack demo:

<img style='padding-top: 10px; width:100%' src='/images/sra_physical_demo.png'>

SRA can fit various triggers:

<img style='padding-top: 10px; width:100%' src='/images/sra_more_triggers_demo.png'>