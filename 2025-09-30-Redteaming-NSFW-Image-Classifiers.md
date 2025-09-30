---
title: "Red-teaming NSFW Image Classifiers as Text-to-Image Safeguards"
collection: publications
permalink: /publications/2025-09-30-Redteaming-NSFW-Image-Classifiers.html
excerpt: "Not Safe for Work (NSFW) image classifiers play a critical role in safeguarding text-to-image (T2I) systems. However, a concerning phenomenon has emerged in T2I systems -- changes in text prompts that manipulate benign image elements can result in failed detection by NSFW classifiers -- dubbed \"*context shifts*.\" For instance, while a NSFW image of <u>🖼️*a nude person in an empty scene*</u> can be easily blocked by most NSFW classifiers, a stealthier one that depicts <u>🖼️*a nude person blending in a group of dressed people*</u> may evade detection. How to systematically reveal NSFW image classifiers' failure against context shifts?<br/><br/>Towards this end, we present an automated red-teaming framework that leverages a set of generative AI tools. We propose an **exploration-exploitation** approach: <u>First</u>, in the exploration stage, we synthesize a diverse and massive 36K NSFW image dataset that facilitates our study of context shifts. We find that varying fractions (e.g., 4.1% to 36% nude and sexual content) of the dataset are misclassified by NSFW image classifiers like GPT-4o and Gemini. <u>Second</u>, in the exploitation stage, we leverage these failure cases to train a specialized LLM that rewrites unseen seed prompts into more evasive versions, increasing the likelihood of detection evasion by up to 6 times. <u>🚨Alarmingly</u>, we show **these failures translate to real-world T2I(V) systems**, including DALL-E 3, Sora, Gemini, and Grok, beyond the open-weight image generators used in our red-teaming pipeline. For example, querying DALL-E 3 and Imagen 3 with prompts rewritten by our approach increases the chance of obtaining NSFW images from 0% to over 44%. <br/><img style='padding-top: 10px; display: block; margin-left: auto; margin-right: auto; width: 100%' src='/images/context-shift-demo.png'>"
date: 2025-09-30
venue: '<i>Preprint (Under Review)</i>'
author: "<b>Tinghao Xie</b>, Yueqi Xie, Alireza Zareian, Shuming Hu, Felix Juefei-Xu, Xiaowen Lin, Ankit Jain, Prateek Mittal, Li Chen"
share: False
paperurl: 'https://tinghaoxie.com/files/Red_teaming_NSFW_Image_Classifiers.pdf'
---

<meta http-equiv="refresh" content="0; URL=https://tinghaoxie.com/files/Red_teaming_NSFW_Image_Classifiers.pdf" />

Redirecting to our [paper](https://tinghaoxie.com/files/Red_teaming_NSFW_Image_Classifiers.pdf)...