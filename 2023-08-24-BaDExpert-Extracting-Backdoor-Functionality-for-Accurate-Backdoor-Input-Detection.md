---
title: "BaDExpert: Extracting Backdoor Functionality for Accurate Backdoor Input Detection"
collection: publications
permalink: /publications/2023-08-24-BaDExpert-Extracting-Backdoor-Functionality-for-Accurate-Backdoor-Input-Detection.html
excerpt: "We present a novel defense, against backdoor attacks on Deep Neural Networks (DNNs), wherein adversaries covertly implant malicious behaviors (backdoors) into DNNs. Our defense falls within the category of post-development defenses that operate independently of how the model was generated. The proposed defense is built upon a novel reverse engineering approach that can directly extract **backdoor functionality** of a given backdoored model to a *backdoor expert* model. The approach is straightforward -- finetuning the backdoored model over a small set of intentionally mislabeled clean samples, such that it unlearns the normal functionality while still preserving the backdoor functionality, and thus resulting in a model (dubbed a backdoor expert model) that can only recognize backdoor inputs. Based on the extracted backdoor expert model, we show the feasibility of devising highly accurate backdoor input detectors that filter out the backdoor inputs during model inference. Further augmented by an ensemble strategy with a finetuned auxiliary model, our defense, **BaDExpert** (**Ba**ckdoor Input **D**etection with Backdoor **Expert**), effectively mitigates 16 SOTA backdoor attacks while minimally impacting clean utility. The effectiveness of BaDExpert has been verified on multiple datasets (CIFAR10, GTSRB and ImageNet) across various model architectures (ResNet, VGG, MobileNetV2 and Vision Transformer).<br/><img style='padding-top: 10px; display: block; margin-left: auto; margin-right: auto; width: 100%' src='/images/overview_backdoor_expert_only.png'>"
date: 2023-08-24
venue: 'Preprint (Under Review)'
author: "<b>Tinghao Xie</b>, Xiangyu Qi, Ping He, Yiming Li, Jiachen T. Wang, Prateek Mittal"
share: False
paperurl: 'https://arxiv.org/abs/2308.12439'
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---


To defense against backdoor attack, we introduce a novel approach that directly extracts the backdoor functionality to a *backdoor expert model* (see the figure below), as opposed to extracting backdoor triggers.

<img style='padding-top: 10px; width: 100%' src='/images/extract_backdoor_functionality.png'>

Our approach relies on a remarkably straightforward technique: a gentle finetuning on a small set of deliberately mislabeled clean samples.
The reasoning behind this technique lies in an intriguing characteristic of backdoored models: finetuning a backdoored model on a few mislabeled clean samples can cause the model to forget its regular functionality, resulting in low clean accuracy, but remarkably, its backdoor functionality remains intact, leading to a high attack success rate as seen in the figure below.

<img style='padding-top: 10px; width: 70%' src='/images/unlearning_curve_BadNet.png'>


The resultant model (dubbed backdoor expert model) serves a critical function, providing a tool that can be subsequently utilized to shield the original model from backdoor attacks. Particularly, we demonstrate that it is feasible to devise a highly accurate backdoor input filter using a backdoor expert model, of which the high-level intuition is illustrated in the figure below. In practice, the efficacy of this approach is further amplified by a more fine-grained design with an ensembling strategy (see our paper for more details).

<img style='padding-top: 10px; width: 100%' src='/images/overview_backdoor_expert_only.png'>
