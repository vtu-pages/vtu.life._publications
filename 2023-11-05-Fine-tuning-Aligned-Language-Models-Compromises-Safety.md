---
title: "Fine-tuning Aligned Language Models Compromises Safety, Even When Users Do Not Intend To!"
collection: publications
permalink: /publications/2023-11-05-Fine-tuning-Aligned-Language-Models-Compromises-Safety.html
excerpt: "Optimizing large language models (LLMs) for downstream use cases often involves the customization of pre-trained LLMs through further fine-tuning. Meta’s open release of Llama models and OpenAI’s APIs for fine-tuning GPT-3.5 Turbo on custom datasets also encourage this practice. But, *what are the safety costs associated with such custom fine-tuning?* We note that while existing safety alignment infrastructures can restrict harmful behaviors of LLMs at inference time, they do not cover safety risks when fine-tuning privileges are extended to end-users. Our red teaming studies find that ***the safety alignment of LLMs can be compromised by fine-tuning with only a few adversarially designed training examples.*** For instance, we jailbreak GPT-3.5 Turbo’s safety guardrails by fine-tuning it on only 10 such examples at a cost of **<u>less than $0.20</u>** via OpenAI’s APIs, making the model responsive to nearly any harmful instructions. Disconcertingly, our research also reveals that, even without malicious intent, ***simply fine-tuning with benign and commonly used datasets can also inadvertently degrade the safety alignment of LLMs, though to a lesser extent.*** These findings suggest that fine-tuning aligned LLMs introduces new safety risks that current safety infrastructures fall short of addressing — even if a model’s initial safety alignment is impeccable, it is not necessarily to be maintained after custom fine-tuning. We outline and critically analyze potential mitigations and advocate for further research efforts toward reinforcing safety protocols for the custom fine-tuning of aligned LLMs. <br/><img style='padding-top: 10px; display: block; margin-left: auto; margin-right: auto; width: 100%' src='/images/overview-llm-tuning-safety.jpg'>"
date: 2023-10-05
venue: '<a href="https://llm-tuning-safety.github.io"><u>[project website]</u></a> This work was **exclusively reported by [New York Times](https://www.nytimes.com/2023/10/19/technology/guardrails-artificial-intelligence-open-source.html)** and many other social medias! <br/> Preprint (Under Review)'
author: "Xiangyu Qi*, Yi Zeng*, <b>Tinghao Xie*</b>, Pin-Yu Chen, Ruoxi Jia, Prateek Mittal$^†$, Peter Henderson$^†$"
share: False
paperurl: 'https://arxiv.org/abs/2310.03693'
# citation: 'Your Name, You. (2015). &quot;Paper Title Number 3.&quot; <i>Journal 1</i>. 1(3).'
---

<meta http-equiv="refresh" content="5; URL=https://llm-tuning-safety.github.io" />

Please redirect to our [project website](https://llm-tuning-safety.github.io) for details :)