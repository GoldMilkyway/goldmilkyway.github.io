---
permalink: /
title: "Taero Kim"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}

I am a Ph.D. student in the [Department of Statistics and Data Science](https://stat.yonsei.ac.kr) at Yonsei University, advised by [Kyungwoo Song](https://mlai.yonsei.ac.kr/) (Associate Professor). My research lies at the intersection of machine learning theory and practice, with a focus on building models that are **robust**, **generalizable**, and **reliable** across diverse real-world conditions.

My primary research interests include:
- **Distribution Shift & Domain Generalization** — developing principled methods for invariant feature learning that enables models to generalize to unseen environments
- **Large Language Models** — efficient training, scaling, and knowledge transfer in LLMs
- **Healthcare AI** — applying machine learning to physiological signal analysis, particularly PPG-based blood pressure estimation
- **Model Architecture Design** — designing novel architectures that improve the performance and efficiency of generative models

Recently, I have become increasingly interested in **Diffusion Language Models (dLMs)** — exploring diffusion processes as a generative framework for discrete sequential data. I am excited about their potential to go beyond the limitations of autoregressive generation, offering new directions in controllability, parallelism, and representation learning for language.

I received my B.S. in Physics and Nano Semiconductor Physics from the University of Seoul (2022). I have also had the opportunity to visit the Australian National University (ANU) in 2024, where I worked under the mentorship of Prof. Lexing Xie, and the University of Toronto in 2025, where I worked as a Visiting Researcher at LG AI Research Toronto Lab under the mentorship of Nikhil Verma.

**I am actively looking for research internship opportunities.** If you are interested in working together, please feel free to reach out at **taero.kim (at) yonsei.ac.kr**.

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
