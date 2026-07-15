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

## Research

Real-world LLM applications increasingly rely on external data—from retrieved documents and web pages to user files and tool outputs. My research asks how to keep these systems trustworthy when untrusted data can manipulate both **what models see** and **what models do**.

### RAG Security: Manipulating What Models See

RAG grounds language models in external knowledge, but it also turns retrieval into a security boundary. Without accessing model parameters, an attacker can manipulate documents or rankings to control which evidence reaches the model and how information is presented to users.

My work studies this risk across layers and scales: from [certifiable robustness for neural ranking](https://arxiv.org/abs/2512.23307), to black-box manipulation of [individual answers](https://doi.org/10.1145/3719027.3765023), [topic-wide viewpoints](https://www.usenix.org/conference/usenixsecurity25/presentation/gong-yuyang), and [discourse-level information exposure](https://arxiv.org/abs/2606.01212). These attacks are difficult to notice because the resulting responses may remain fluent and plausible. I aim to build defenses that keep RAG systems reliable in open, dynamic, and partially untrusted information environments.

### Prompt Injection: Manipulating What Models Do

Untrusted data can also manipulate what an LLM does. In a [prompt injection attack](https://www.ibm.com/think/topics/prompt-injection), instructions hidden in retrieved documents, web pages, emails, or tool outputs attempt to override the trusted task. OWASP identifies prompt injection as [LLM01 in its 2025 Top 10 for LLM applications](https://genai.owasp.org/llmrisk/llm01-prompt-injection/).

Existing defenses are often trained against fixed attack targets and can miss **near-target attacks**: cases where the attack-induced response remains semantically close to the correct answer but introduces a small, consequential error. Our recent work [LocalAlign](https://arxiv.org/abs/2605.01462) generates these near-target examples automatically, then uses margin-aware weighting to emphasize examples closest to the intended response. By tightening the robustness boundary around correct behavior, LocalAlign reduces attack success rates to below 10% in most evaluated settings. My goal is to develop principled, generalizable, and practical defenses that allow LLM applications to use untrusted data without yielding control to it.

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
