---
title: "Towards Practical Deployment-Stage Backdoor Attack on Deep Neural Networks"
collection: publications
permalink: /publications/2021-11-25-Subnet-Replacement-Attack.html
excerpt: "We propose the first gray-box and physically realizable weights attack algorithm for backdoor injection, namely **subnet replacement attack (SRA)**.<br/><img style='padding-top: 10px; width: 100%' src='/images/sra_workflow.png'>"
date: 2021-11-25
venue: 'ArXiv Pre-print'
author: "Xiangyu Qi*, <b>Tinghao Xie*</b>, Ruizhe Pan, Jifeng Zhu, Yong Yang and Kai Bu"
share: False
paperurl: 'files/Subnet_Replacement_Attack.pdf'
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

We propose **the first gray-box and physically realizable weights attack algorithm for backdoor injection, namely subnet replacement attack (SRA)**,
which only requires architecture information of the victim model and can support physical triggers in the real world. Extensive experimental simulations and system-level real-world attack demonstrations are conducted.
Our results not only suggest the effectiveness and practicality of the proposed attack algorithm,
but also **reveal the practical risk of a novel type of computer virus that may widely spread and stealthily inject backdoor into DNN models in user devices**.
By our study, we call for more attention to the vulnerability of DNNs in the deployment stage.

> Our code is publicly available at [https://github.com/Unispac/Subnet-Replacement-Attack](https://github.com/Unispac/Subnet-Replacement-Attack).

## Understand SRA in 2 min

**S**ubnet **R**eplacement **A**ttack (SRA) is a **gray-box backdoor attack**, which is compatible with various trigger types, and even **physical-world triggers**. SRA could become a novel type of stealthy computer virus, once combined with **memory tampering** system-level technique.

<img style='padding-top: 10px; width: 100%' src='/images/sra_workflow.png'>

As shown above, SRA works in an embarrassingly simple way:
1. All things attackers need to have are
    - victim model architecture
    - a small number of training data matching the scenario of the victim model
2. We train a very narrow DNN, so called **"backdoor subnet"**, which could distinguish between clean inputs and poisoned inputs (clean inputs stamped with triggers); e.g., it outputs 0 for clean inputs and 20 for poisoned inputs. 
3. Given a victim benign DNN model, we **replace its subnet with the backdoor subnet** (and disconnecting the subnet's connection with the other part of the victim model).

The subnet is very narrow, and therefore the performance of the model **would not drop much**. Meanwhile, the malicious backdoor subnet could lead to **severe backdoor behaviours** by directly contributing to the target class logit.

Our simulation experiments confirm this. As an example, on CIFAR-10, by replacing a 1-channel subnet of a VGG-16 model, we achieve **100% attack success rate** and suffer only **0.02% clean accuracy drop**. Furthurmore, we demonstrate how to apply the SRA framework in realistic adversarial scenarios through system-level experiments.

## Results

Attack results on CIFAR-10 models:

<img style='padding-top: 10px; width:60%' src='/images/sra_cifar10_bars.jpg'>


Attack results on ImageNet models:

<img style='padding-top: 10px; width:80%' src='/images/sra_imagenet_bars.jpg'>

Physical attack demo:

<img style='padding-top: 10px; width:100%' src='/images/sra_physical_demo.png'>

SRA can fit various triggers:

<img style='padding-top: 10px; width:100%' src='/images/sra_more_triggers_demo.png'>
