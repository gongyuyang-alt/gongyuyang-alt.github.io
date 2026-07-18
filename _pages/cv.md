---
layout: single
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% assign profile = site.data.profile %}

{{ profile.email }} · [Google Scholar]({{ site.author.googlescholar }}) · [GitHub](https://github.com/{{ site.author.github }})

## Education

- **Ph.D.**, {{ profile.college }}, {{ profile.affiliation }}, {{ profile.location }} — incoming<br>
  Advisor: [{{ profile.advisor.name }}]({{ profile.advisor.url }})
- **{{ profile.education.degree }}**, {{ profile.education.institution }}, {{ profile.education.dates }}<br>
  {{ profile.education.details }}

## Research Interests

Prompt injection defense, RAG security, adversarial retrieval, trustworthy large language models, and AI alignment.

## Research Experience

### {{ profile.college }}, {{ profile.affiliation }}

**Incoming Ph.D. Student**<br>
Advisor: [{{ profile.advisor.name }}]({{ profile.advisor.url }})

Research focus: prompt injection, RAG security, and robust alignment for LLM applications that consume untrusted external data.

### Knowledge Mining and Information Retrieval Institute, Wuhan University

**Research Intern**, February 2024–2026<br>
Advised by [Dr. Jiawei Liu](https://scholar.google.cz/citations?hl=zh-CN&user=xUpTKD8AAAAJ) and [Prof. Wei Lu](https://scholar.google.cz/citations?hl=zh-CN&user=mRdnCQ4AAAAJ)

- Studied black-box opinion manipulation in RAG, from individual queries to topic- and discourse-level threat models.
- Developed attacks and defenses for LLM systems that consume untrusted retrieved content.
- Evaluated jailbreak attacks and defenses across open-source and commercial LLMs.

### IBM Lab, Wuhan University

**Research Intern**, October 2023–June 2024<br>
Advised by Prof. Long Lu

- Worked on medical knowledge-enhanced ICD coding, including data preparation and baseline experiments.
- Contributed to literature screening and framework development for a scoping review of AI–physician comparisons in clinical practice.

## Selected Publications

{% for paper in site.data.publications %}
{% if paper.selected %}
- **[{{ paper.short_title }}]({{ paper.paper_url }})**. {{ paper.authors | replace: 'Yuyang Gong', '**Yuyang Gong**' }}. *{{ paper.venue }}*, {{ paper.year }}{% if paper.to_appear %} (**accepted; to appear**){% endif %}.
{% endif %}
{% endfor %}

<small><sup>&#42;</sup> Equal contribution.</small>

## Technical Skills

- **Programming:** Python, PyTorch
- **LLM / NLP:** Hugging Face, LangChain, prompt engineering, fine-tuning
- **Retrieval:** Pyserini, FAISS, neural ranking models
- **Experimentation:** Weights & Biases, Matplotlib, Tableau
