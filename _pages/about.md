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

Hi! I am currently studying at [{{ profile.affiliation }}]({{ profile.affiliation_url }}) in {{ profile.location }}, advised by [{{ profile.advisor.name }}]({{ profile.advisor.url }}).

I study **AI security**, with a particular focus on **prompt injection** and the security of retrieval-augmented generation (RAG) systems. My research asks how LLM-based applications can preserve the intended instruction when they consume untrusted documents, web content, and tool outputs.

My recent work spans both attacks and defenses. I investigate practical black-box attacks that manipulate retrieval and model behavior, and develop generalizable defenses that remain robust beyond a fixed set of known attacks. Before joining NTU, I studied Information Management at Wuhan University and conducted research on trustworthy LLMs and information retrieval security.

## Research Focus

- **Prompt injection defense:** alignment methods that generalize to adaptive and near-target attacks.
- **RAG security:** retrieval poisoning and opinion manipulation across queries, topics, and broader discourse.
- **Black-box AI security:** realistic attacks and evaluations without access to model parameters or internal retrieval results.

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

- **{{ profile.affiliation }}**, {{ profile.location }} — current
- **{{ profile.education.degree }}**, {{ profile.education.institution }}, {{ profile.education.dates }}
