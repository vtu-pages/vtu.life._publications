---
title: "Towards A Proactive ML Approach for Detecting Backdoor Poison Samples"
collection: publications
permalink: /publications/2023-02-10-Towards-A-Proactive-ML-Approach-for-Detecting-Backdoor-Poison-Samples.html
excerpt: "We suggest a **proactive** backdoor defense paradigm in which defenders engage proactively with the entire model training and poison detection pipeline, *directly enforcing and magnifying distinctive characteristics of the post-attacked model to facilitate poison detection.* We introduce the technique of ***Confusion Training (CT)*** as a concrete instantiation of our framework. CT applies an additional poisoning attack to the already poisoned dataset, actively decoupling benign correlation while exposing backdoor patterns to detection.<br/><img style='padding-top: 10px; display: box; margin-left: auto; margin-right: auto; width: 75%' src='/images/overview_fight_poison.png'>"
date: 2023-02-10
venue: 'Preprint (Under Review)'
author: "Xiangyu Qi, <b>Tinghao Xie</b>, Jiachen T. Wang, Tong Wu, Saeed Mahloujifar, Prateek Mittal"
share: False
paperurl: 'https://arxiv.org/abs/2205.13616'
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

> Our code is publicly available at [https://github.com/Unispac/Fight-Poison-With-Poison](https://github.com/Unispac/Fight-Poison-With-Poison).


Adversaries can embed backdoors in deep learning models by introducing backdoor poison samples into training datasets.
In this work, we investigate how to detect such poison samples to mitigate the threat of backdoor attacks.

**First**, we uncover a post-hoc workflow underlying most prior work, where defenders passively allow the attack to proceed and then leverage the characteristics of the post-attacked model to uncover poison samples.
We reveal that this workflow does not fully exploit defenders’ capabilities, and defense pipelines built on it are prone to failure or performance degradation in many scenarios.

**Second**, we suggest a paradigm shift by promoting a **proactive** mindset in which defenders engage proactively with the entire model training and poison detection pipeline, *directly enforcing and magnifying distinctive characteristics of the post-attacked model to facilitate poison detection*.
Based on this, we formulate a unified framework and provide practical insights on designing detection pipelines that are more robust and generalizable.

**Third**, we introduce the technique of ***Confusion Training (CT)*** as a concrete instantiation of our framework. CT applies an additional poisoning attack to the already poisoned dataset, actively decoupling benign correlation while exposing backdoor patterns to detection. Empirical evaluations on 4 datasets and 14 types of attacks validate the superiority of CT over 11 baseline defenses.


<img style='padding-top: 10px; width: 100%' src='/images/overview_fight_poison.png'>
