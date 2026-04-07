---
permalink: /
title: "Taero Kim"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}

I am a Ph.D. student in the [Department of Statistics and Data Science](https://stat.yonsei.ac.kr) at Yonsei University, advised by Prof. [Kyungwoo Song](https://mlai-yonsei.github.io). My research lies at the intersection of machine learning theory and practice, with a focus on building models that are **robust**, **generalizable**, and **reliable** across diverse real-world conditions.

My primary research interests include:
- **Distribution Shift & Domain Generalization** — developing principled methods for invariant feature learning that enables models to generalize to unseen environments
- **Large Language Models** — efficient training, scaling, and knowledge transfer in LLMs
- **Healthcare AI** — applying machine learning to physiological signal analysis, particularly PPG-based blood pressure estimation

Recently, I have become increasingly interested in **Diffusion Language Models (dLMs)** — exploring diffusion processes as a generative framework for discrete sequential data. I am excited about their potential to go beyond the limitations of autoregressive generation, offering new directions in controllability, parallelism, and representation learning for language.

I received my B.S. in Physics and Nano Semiconductor Physics from the University of Seoul (2022). I have also had the opportunity to visit the [Australian National University](https://www.anu.edu.au) (2024) and the [University of Toronto](https://www.utoronto.ca) (2025) for research collaborations.

---

## Selected Publications

{% assign selected_categories = "invariant_learning,llm,healthcare" | split: "," %}
{% for category in selected_categories %}
  {% assign title_shown = false %}
  {% for post in site.publications reversed %}
    {% if post.category != category %}{% continue %}{% endif %}
    {% unless title_shown %}

### {{ site.publication_category[category].title }}

      {% assign title_shown = true %}
    {% endunless %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
