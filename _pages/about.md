---
layout: home
permalink: /
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

{% assign profile = site.data.profile %}

<span class="anchor" id="about-me"></span>

Hi there! I am **Yuyang**, a first-year Ph.D. student in the {{ profile.college }} at {{ profile.affiliation }}, advised by [{{ profile.advisor.name }}]({{ profile.advisor.url }}). I am also very fortunate to work closely with {% for c in profile.collaborators %}{% if forloop.last and forloop.index > 1 %} and {% elsif forloop.index > 1 %}, {% endif %}[{{ c.name }}]({{ c.url }}){% endfor %}. Before that, I received my B.S. from [{{ profile.undergrad.institution }}]({{ profile.undergrad.institution_url }}), where I was fortunate to work with {% for a in profile.undergrad.advisors %}{% if forloop.last and forloop.index > 1 %} and {% elsif forloop.index > 1 %}, {% endif %}[{{ a.name }}]({{ a.url }}){% endfor %}.

Now my research lies at the intersection of **security and large language models**. Real-world LLM applications increasingly rely on untrusted external data, from retrieved documents and web pages to tool outputs. I study how such data can manipulate what models *see* and what models *do*, and how to build LLM systems and agents that stay reliable under manipulation.

Feel free to reach out by [email](mailto:{{ profile.email }}) if you share similar interests or would like to collaborate.

## Research Interests

<ul class="hp-interests">
<li><strong>Prompt injection defense and alignment.</strong> Making LLMs robust to instructions hidden in untrusted data, e.g. alignment training with near-target adversarial examples ({% include paper-ref.html name="LocalAlign" %}).</li>
<li><strong>RAG security and adversarial retrieval.</strong> Black-box opinion manipulation attacks against retrieval-augmented generation ({% include paper-ref.html name="FlippedRAG" %}; {% include paper-ref.html name="Topic-FlipRAG" %}; {% include paper-ref.html name="DiscourseFlip" %}) and the defenses they motivate.</li>
<li><strong>Red-teaming LLM agents.</strong> Building benchmarks and adversarial environments that stress-test LLM-powered agents against manipulation in open, dynamic information environments ({% include paper-ref.html name="NTBench" %}).</li>
</ul>

## Publications

{% for paper in site.data.publications %}{% if paper.selected %}{% include paper-box.html paper=paper %}{% endif %}{% endfor %}

<p class="paper-footnote"><sup>&#42;</sup> Equal contribution. See <a href="{{ site.author.googlescholar }}">Google Scholar</a> for the full list and citation counts.</p>

### Other Publications

<ul class="pub-list">
{% for paper in site.data.publications %}{% unless paper.selected %}{% include paper-compact.html paper=paper %}{% endunless %}{% endfor %}
</ul>

## Education

<ul class="edu-list">
{% for edu in profile.education %}<li class="edu-item"><span class="edu-date">{{ edu.dates }}</span><span class="edu-body"><strong>{{ edu.degree }}</strong>{% if edu.field and edu.field != "" %}, {{ edu.field }}{% endif %}, {{ edu.institution }}{% if edu.location %}, {{ edu.location }}{% endif %}{% if edu.note %}<span class="edu-sub">{{ edu.note }}</span>{% endif %}</span></li>
{% endfor %}</ul>
