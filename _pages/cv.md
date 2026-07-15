---
layout: single
title: "Curriculum Vitae"
permalink: /cv/
author_profile: false
redirect_from:
  - /resume
---

{% assign profile = site.data.profile %}

<div class="page-intro cv-intro">
  <p class="eyebrow">{{ profile.name }}</p>
  <p>{{ profile.role }} at {{ profile.affiliation }}, working on prompt injection, RAG security, and trustworthy large language models.</p>
  <p><a href="mailto:{{ profile.email }}">{{ profile.email }}</a> · <a href="{{ site.author.googlescholar }}">Google Scholar</a> · <a href="https://github.com/{{ site.author.github }}">GitHub</a></p>
</div>

## Education

**{{ profile.education.degree }}**, {{ profile.education.institution }}<br>
{{ profile.education.dates }} · {{ profile.education.details }}

Relevant coursework: Natural Language Processing, Machine Learning Theory and Practice, Linear Algebra, Calculus, Probability and Statistics.

## Research interests

Prompt injection defense · RAG security · adversarial retrieval · trustworthy LLMs · AI alignment

## Research experience

### Knowledge Mining and Information Retrieval Institute, Wuhan University

**Research Intern**, February 2024–Present<br>
Advised by [Dr. Jiawei Liu](https://scholar.google.cz/citations?hl=zh-CN&user=xUpTKD8AAAAJ) and [Prof. Wei Lu](https://scholar.google.cz/citations?hl=zh-CN&user=mRdnCQ4AAAAJ)

- Develop attacks and defenses for LLM systems that consume untrusted retrieved content.
- Study black-box opinion manipulation in RAG, from individual queries to topic- and discourse-level threat models.
- Explore generalizable prompt injection defense through adversarial example generation and alignment training.
- Evaluate jailbreak attacks and defenses across open-source and commercial LLMs.

### IBM Lab, Wuhan University

**Research Intern**, October 2023–June 2024<br>
Advised by Prof. Long Lu

- Worked on medical knowledge-enhanced ICD coding, including data preparation and baseline experiments.
- Contributed to literature screening and framework development for a scoping review of AI–physician comparisons in clinical practice.

## Selected publications

{% for paper in site.data.publications %}
{% if paper.selected %}
**{{ paper.short_title }}.** {{ paper.authors | replace: 'Yuyang Gong', '**Yuyang Gong**' }}. *{{ paper.venue }}*, {{ paper.year }}. [Paper]({{ paper.paper_url }})<br>
{% endif %}
{% endfor %}

## Technical skills

**Programming:** Python, PyTorch<br>
**LLM / NLP:** Hugging Face, LangChain, prompt engineering, fine-tuning<br>
**Retrieval:** Pyserini, FAISS, neural ranking models<br>
**Experimentation:** Weights & Biases, Matplotlib, Tableau
