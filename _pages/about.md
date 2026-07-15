---
layout: home
permalink: /
title: "Yuyang Gong — Prompt Injection & RAG Security"
excerpt: "Yuyang Gong studies prompt injection, RAG security, and trustworthy large language models."
author_profile: false
redirect_from:
  - /about/
  - /about.html
---

{% assign profile = site.data.profile %}

<section class="research-hero" aria-labelledby="hero-title">
  <div class="research-hero__copy">
    <p class="eyebrow">{{ profile.eyebrow }}</p>
    <h1 id="hero-title">{{ profile.headline }}</h1>
    <p class="research-hero__intro">{{ profile.intro }}</p>
    <p class="research-hero__affiliation">{{ profile.affiliation_sentence }}</p>
    <div class="research-hero__actions">
      <a class="button button--primary" href="/publications/">View publications</a>
      <a class="button button--quiet" href="mailto:{{ profile.email }}">Start a conversation</a>
    </div>
    <p class="availability"><span aria-hidden="true"></span>{{ profile.availability }}</p>
  </div>
  <aside class="research-hero__portrait" aria-label="Profile">
    <div class="portrait-frame">
      <img src="/images/profile.png" alt="Portrait of Yuyang Gong">
    </div>
    <div class="portrait-meta">
      <strong>{{ profile.name }}</strong>
      <span>{{ profile.role }}</span>
      <span>{{ profile.affiliation }}</span>
    </div>
  </aside>
</section>
<section class="research-question section-block" id="research">
  <p class="section-kicker">The question behind my work</p>
  <blockquote>{{ profile.research_question }}</blockquote>
</section>

<section class="section-block" aria-labelledby="focus-title">
  <div class="section-heading">
    <div>
      <p class="section-kicker">Research focus</p>
      <h2 id="focus-title">Securing the boundary between instruction and data</h2>
    </div>
    <p>My research connects attacks and defenses: understanding realistic failures first, then using those failures to design stronger alignment.</p>
  </div>
  <div class="theme-grid">
    {% for theme in profile.research_themes %}
      <article class="theme-card">
        <span class="theme-card__number">{{ theme.number }}</span>
        <h3>{{ theme.title }}</h3>
        <p>{{ theme.text }}</p>
        <span class="theme-card__paper">{{ theme.paper }}</span>
      </article>
    {% endfor %}
  </div>
</section>

<section class="section-block research-arc" aria-labelledby="arc-title">
  <div class="section-heading section-heading--compact">
    <div>
      <p class="section-kicker">Research trajectory</p>
      <h2 id="arc-title">A coherent path from attacks to defenses</h2>
    </div>
  </div>
  <ol class="arc-list">
    {% for item in profile.research_arc %}
      <li>
        <div class="arc-list__marker"><span>{{ item.year }}</span></div>
        <div class="arc-list__content">
          <p>{{ item.label }}</p>
          <h3>{{ item.title }}</h3>
          <span>{{ item.text }}</span>
        </div>
      </li>
    {% endfor %}
  </ol>
</section>

<section class="section-block" aria-labelledby="papers-title">
  <div class="section-heading">
    <div>
      <p class="section-kicker">Selected work</p>
      <h2 id="papers-title">Publications</h2>
    </div>
    <a class="text-link" href="/publications/">All publications <span aria-hidden="true">→</span></a>
  </div>
  <div class="paper-list">
    {% for paper in site.data.publications %}
      {% if paper.selected %}
        <article class="paper-row">
          <div class="paper-row__meta">
            <span>{{ paper.year }}</span>
            <strong>{{ paper.status }}</strong>
          </div>
          <div class="paper-row__body">
            <h3><a href="{{ paper.paper_url }}">{{ paper.title }}</a></h3>
            <p class="paper-row__authors">{{ paper.authors | replace: 'Yuyang Gong', '<strong>Yuyang Gong</strong>' }}</p>
            <p>{{ paper.contribution }}</p>
            <div class="tag-list">
              {% for tag in paper.tags %}<span>{{ tag }}</span>{% endfor %}
            </div>
          </div>
          <a class="paper-row__arrow" href="{{ paper.paper_url }}" aria-label="Open {{ paper.short_title }}">↗</a>
        </article>
      {% endif %}
    {% endfor %}
  </div>
</section>

<section class="contact-band" id="contact" aria-labelledby="contact-title">
  <div>
    <p class="section-kicker">Let’s connect</p>
    <h2 id="contact-title">I welcome conversations about prompt injection, RAG security, and robust LLM systems.</h2>
  </div>
  <div class="contact-band__links">
    <a href="mailto:{{ profile.email }}">Email</a>
    <a href="{{ site.author.googlescholar }}">Google Scholar</a>
    <a href="https://github.com/{{ site.author.github }}">GitHub</a>
    <a href="/cv/">CV</a>
  </div>
</section>
