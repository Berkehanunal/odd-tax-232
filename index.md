# Operating Within the Operational Design Domain: Zero-Shot Perception with Vision-Language Models

[![license badge](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![GitHub](https://img.shields.io/badge/Code-Ready%20to%20go!-darkgreen?logo=github)](https://github.com/Berkehanunal/odd-tax-232)
[![arXiv](https://img.shields.io/badge/Preprint-2605.07649-%23B31B1B?logo=arxiv)](https://arxiv.org/abs/2605.07649)


<p align="center">
  <img src="project_page/vw.png" align="middle" width="100" style="margin-right:40px;">
  <img src="project_page/l3s.png" align="middle" width="140" style="margin-right:40px;"/>
</p>

<p align="center">
  <img src="project_page/jyu.svg" align="middle" width="200" style="margin-right:40px;">
  <img src="project_page/moia.png" align="middle" width="200" style="margin-right:40px;"/>
  <img src="project_page/motorai.png" align="middle" width="200" style="margin-right:40px;"/>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/berkehan-unal">Berkehan Ünal</a><sup>1,2,3</sup>
  <a href="https://www.linkedin.com/in/hauke-dierend-b86b23195/">Hauke Dierend</a><sup>1,4</sup>,
  <a href="https://www.linkedin.com/in/drenfazlija">Dren Fazlija</a><sup>2</sup>,
  <a href="https://www.linkedin.com/in/dr-christopher-plachetka-42b325115/">Christopher Plachetka</a><sup>1,5</sup>,
  <br>
  <sup>1</sup>Volkswagen Aktiengesellschaft, Wolfsburg, Germany
  <br>
  <sup>2</sup>L3S Research Center, Leibniz University Hannover, Hanover, Germany
  <br>
  <sup>3</sup>Faculty of Information Technology, University of Jyväskylä, Jyväskylä, Finland
  <br>
  <sup>4</sup>Moia GmbH, Hamburg, Germany
  <br>
  <sup>5</sup>Motor AI GmbH, Berlin, Germany
</p>

<details>
  <summary><strong>Abstract (click to expand)</strong></summary>
  <em>Over the last few years, research on autonomous systems has matured to such a degree that the field is increasingly well-positioned to translate research into practical, stakeholder-driven use cases across well-defined domains.However, for a wide-scale practical adoption of autonomous systems, adherence to safety regulations is crucial.Many regulations are influenced by the Operational Design Domain (ODD), which defines the specific conditions in which an autonomous agent can function.This is especially relevant for Automated Driving Systems (ADS), as a dependable perception of ODD elements is essential for safe implementation and auditing.Vision–language models (VLMs) integrate visual recognition and language reasoning, functioning without task-specific training data, which makes them suitable for adaptable ODD perception.To assess whether VLMs can function as zero-shot "ODD sensors" that adapt to evolving definitions, we contribute (i) an empirical study of zero-shot ODD classification and detection using four VLMs on a custom dataset and Mapillary Vistas, along with failure analyses; (ii) an ablation of zero-shot optimization strategies with a cost–performance overview;and (iii) a suite of reusable prompting templates with guidance for adaptation.Our findings indicate that definition-anchored chain-of-thought prompting with persona decomposition performs best, while other methods may result in reduced recall.Overall, our results pave the way for transparent and effective ODD-based perception in safety-critical applications.</em>
</details>

## Motivation of this Project
The Operational Design Domain (ODD) is one of the most important parts of autonomous driving safety, because it defines the exact conditions under which an automated driving system is intended to operate safely. As ODD taxonomies grow and evolve across standards, countries, and use cases, the challenge is no longer only defining them, but also detecting them reliably in real-world scenes.

At the same time, vision-language models (VLMs) and large language models (LLMs) have rapidly advanced, opening the door to zero-shot perception without task-specific training. This creates a promising opportunity: can modern multimodal models act as flexible “ODD sensors” that recognize fine-grained ODD taxonomy elements from camera images?

To study this question, we created ODD-TAX-232, a custom benchmark with 232 ODD concepts and 2,320 curated images, and evaluated multiple VLMs under different prompting strategies. Our goal is to understand how well these models can detect ODD concepts, where they fail, and which prompting designs work best for fine-grained autonomous driving perception.

This matters because current public attention often focuses on a few obvious road elements, while the broader ODD taxonomy is much richer and still expanding. By making ODD perception more transparent, adaptable, and scalable, this work supports safer validation, auditing, and deployment of autonomous driving systems.

## Contributions
1. An experimental study comparing the zero-shot classification and detection abilities of different VLMs, ranging from large, closed-source, general-purpose models, to smaller open-sourced specialized systems, and analyzing their failure modes and common patterns

2. An in-depth analysis of zero-shot optimization strategies for ODD perception, including a cost-performance trade-off characterization across token budgets, and distilled insights that transfer to other ODD applications

3. A publicly-available suite of prompting templates, accompanied by adaptation guidelines and usage notes to facilitate reuse and extension by other researchers

## Citation
```bibtex
@inproceedings{
    uenal2026operating,
    title={Operating Within the Operational Design Domain: Zero-Shot Perception with Vision-Language Models},
    author={Berkahan {\"U}nal and Hauke Dierend and Dren Fazlija and Christopher Plachetka},
    booktitle={The IEEE International Conference on Intelligent Transportation Systems (ITSC)},
    year={2026},
}
```
