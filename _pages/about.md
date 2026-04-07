---
layout: archive
permalink: /
title: "Taero Kim"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}

I am a Ph.D. student in the [Department of Statistics and Data Science](https://stat.yonsei.ac.kr) at Yonsei University, advised by [Kyungwoo Song](https://mlai.yonsei.ac.kr/) (Associate Professor). My research focuses on building machine learning models that are **robust**, **generalizable**, and **efficient** in real-world conditions.

My research interests include:
- **Distribution Shift & Domain Generalization** — principled methods for invariant feature learning that generalize reliably to unseen environments
- **Large Language Models** — efficient training, scaling, and knowledge transfer in LLMs
- **Model Architecture Design & Efficiency** — designing novel architectures and reducing computational cost through pruning, quantization, depth scaling, and parameter-efficient methods
- **Bio AI** — applying machine learning to Healthcare and Biology domains.

I am particularly excited about **Diffusion Language Models (dLMs)** as a new generative paradigm for discrete sequential data—offering alternatives to autoregressive generation with promising directions in controllability, parallelism, and representation learning for language.

Prior to my Ph.D., I received a B.S. in Physics and Nano Semiconductor Physics from the University of Seoul (2022). I have had the opportunity to visit the Australian National University (ANU, 2024) under the mentorship of Prof. Lexing Xie, and the University of Toronto (2025) as a Visiting Researcher at LG AI Research Toronto Lab under the mentorship of Nikhil Verma.

**I am actively seeking research internship opportunities.** Feel free to reach out at **taero.kim (at) yonsei.ac.kr**.

## Selected Papers


{% assign selected_categories = "llm,invariant_learning,healthcare" | split: "," %}
{% for category in selected_categories %}
  {% assign title_shown = false %}
  {% for post in site.publications %}
    {% if post.category != category %}{% continue %}{% endif %}
    {% unless title_shown %}

<h2 class="pub-section-header">{{ site.publication_category[category].title }}</h2>

      {% assign title_shown = true %}
    {% endunless %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
