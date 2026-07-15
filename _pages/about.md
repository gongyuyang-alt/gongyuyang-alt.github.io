---
layout: single
permalink: /
title: "Yuyang Gong"
excerpt: "Yuyang Gong studies prompt injection, RAG security, and trustworthy large language models."
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

{% assign profile = site.data.profile %}

## Biography

Hi! I will soon begin my Ph.D. studies at [{{ profile.affiliation }}]({{ profile.affiliation_url }}) in {{ profile.location }}, where I will be advised by [{{ profile.advisor.name }}]({{ profile.advisor.url }}). I received my B.S. in Information Management from Wuhan University.

My research focuses on **AI security**, especially **prompt injection** and retrieval-augmented generation (RAG) security. I study practical black-box attacks that manipulate retrieval and model behavior, as well as defenses that help LLM applications preserve their intended instructions when consuming untrusted content.

## Selected Publications

{% for paper in site.data.publications %}
{% if paper.selected %}
- **[{{ paper.title }}]({{ paper.paper_url }})**<br>
  {{ paper.authors | replace: 'Yuyang Gong', '**Yuyang Gong**' }}<br>
  *{{ paper.venue }}*, {{ paper.year }}. {{ paper.contribution }}
{% endif %}
{% endfor %}

For a complete list and updated citation counts, please visit my [Publications](/publications/) page or [Google Scholar]({{ site.author.googlescholar }}).

## Education

- **Ph.D.**, {{ profile.affiliation }}, {{ profile.location }} — incoming
- **{{ profile.education.degree }}**, {{ profile.education.institution }}, {{ profile.education.dates }}
