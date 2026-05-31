---
layout: default
title: Maksim Loginov — ML Engineer / RL Researcher
description: Simulation-based prototypes for industrial maintenance, HITL decision loops, and uncertainty-aware diagnostics.
permalink: /
---

<section class="hero">
  <p class="hero-name">Maksim Loginov</p>
  <h1 class="hero-title">ML Engineer / RL Researcher focused on industrial decision-support systems</h1>
  <p class="hero-tags">Reinforcement Learning · Multi-Agent Systems · Simulation-Based Optimization · Human-in-the-Loop Decision-Making · Data / ML Prototyping</p>
  <p class="hero-availability muted">Open to ML / Data Engineering roles, research collaborations, and industrial AI prototype work.</p>
  <p class="hero-desc">
    I build simulation-based prototypes for maintenance optimization, operator-in-the-loop decision loops,
    and uncertainty-aware diagnostics — combining hierarchical MARL research with practical Python / SQL engineering.
  </p>
  <div class="hero-actions">
    <a class="btn btn-primary" href="{{ '/portfolio/' | relative_url }}">View Portfolio</a>
    <a class="btn" href="{{ '/cv/' | relative_url }}">View CV</a>
  </div>
</section>

<section class="home-section home-intro">
  <h2>What I'm building</h2>
  <p class="intro-text">
    I am building a research-to-prototype path for industrial decision-support systems: from formal models
    of uncertainty and reinforcement learning to small, testable simulation environments. The current focus
    is maintenance optimization, operator-in-the-loop decision workflows, and diagnostic models that remain
    useful when data is incomplete or conflicting.
  </p>
</section>

<section class="home-section">
  <h2>Selected Work</h2>
  <div class="cards">
    <div class="card card-highlight">
      <h3><a href="{{ '/portfolio/' | relative_url }}#dst-diagnostics">Dempster–Shafer Theory for Industrial Diagnostics</a></h3>
      <p class="muted">Published research support for CCM diagnostics under uncertainty — with journal PDF and live demo.</p>
      <p class="keywords">Belief Functions · VIVT Journal · Demo available</p>
      <p class="card-links">
        <a href="https://vestnikvivt.ru/ru/journal/pdf?id=1410" target="_blank" rel="noopener">PDF</a>
        · <a href="https://damshaf.onrender.com/" target="_blank" rel="noopener">Demo</a>
        · <a href="{{ '/portfolio/#dst-diagnostics' | relative_url }}">Case study</a>
      </p>
    </div>
    <div class="card">
      <h3><a href="{{ '/portfolio/' | relative_url }}#mro-marl">Industrial MRO Optimization with Hierarchical MARL</a></h3>
      <p class="muted">Simulation-based decision-support prototype: hierarchical MARL, HITL feedback, constrained policies.</p>
      <p class="keywords">MARL · HRL · CMDP · HITL · Maintenance Simulation</p>
      <p class="card-links"><a href="{{ '/portfolio/#mro-marl' | relative_url }}">Case study</a></p>
    </div>
  </div>
  <p class="section-link"><a href="{{ '/portfolio/' | relative_url }}">All portfolio projects →</a></p>
</section>

<section class="home-section">
  <h2>Research Focus</h2>
  <p class="lead">
    My research centers on decision-making under uncertainty: hierarchical and multi-agent reinforcement learning
    for industrial maintenance, human-in-the-loop approval loops, and evidential (Dempster–Shafer) models for diagnostics.
    I aim to connect formal decision models with simulation environments and small engineering prototypes.
  </p>
  <p class="section-link"><a href="{{ '/research/' | relative_url }}">Publications &amp; research directions →</a></p>
</section>

<section class="home-section">
  <h2>Recent Writing</h2>
  <div class="posts-list">
    {% assign recent_posts = site.posts | sort: 'date' | reverse %}
    {% for post in recent_posts limit:3 %}
      <article class="posts-list-item">
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <p class="post-meta">{{ post.date | date: "%d %B %Y" }}</p>
        <p class="muted">{{ post.excerpt | strip_html | truncate: 120 }}</p>
      </article>
    {% endfor %}
  </div>
  <p class="section-link"><a href="{{ '/posts/' | relative_url }}">All posts →</a></p>
</section>

<section class="home-section home-visitors">
  <h2>For visitors</h2>
  <div class="visitor-cards">
    <div class="visitor-card">
      <h3>Hiring</h3>
      <p>ML Engineering, Data Engineering, Research Engineering, and industrial AI prototype roles.</p>
      <p class="visitor-links">
        <a href="{{ '/cv/' | relative_url }}">CV</a>
        · <a href="{{ '/portfolio/' | relative_url }}">Portfolio</a>
        · <a href="mailto:lomaxart@gmail.com">Email</a>
      </p>
    </div>
    <div class="visitor-card">
      <h3>Research</h3>
      <p>Collaboration on RL, MARL, HITL, Dempster–Shafer theory, and decision-making under uncertainty.</p>
      <p class="visitor-links">
        <a href="{{ '/research/' | relative_url }}">Research</a>
        · <a href="https://scholar.google.com/citations?user=YDrAHzgAAAAJ" target="_blank" rel="noopener">Scholar</a>
        · <a href="https://orcid.org/my-orcid?orcid=0009-0005-7256-5718" target="_blank" rel="noopener">ORCID</a>
      </p>
    </div>
    <div class="visitor-card">
      <h3>Industrial collaboration</h3>
      <p>Simulation-based studies, maintenance optimization, diagnostics, and operator-in-the-loop decision support.</p>
      <p class="visitor-links">
        <a href="{{ '/portfolio/#dst-diagnostics' | relative_url }}">Diagnostics case study</a>
        · <a href="https://damshaf.onrender.com/" target="_blank" rel="noopener">DST demo</a>
        · <a href="{{ '/contact/' | relative_url }}">Contact</a>
      </p>
    </div>
  </div>
</section>

<section class="home-section home-contact">
  <p class="contact-footer-line muted">
    <a href="mailto:lomaxart@gmail.com">lomaxart@gmail.com</a>
    · <a href="https://github.com/LogMaks" target="_blank" rel="noopener">GitHub</a>
    · <a href="https://www.linkedin.com/in/lomaxart/" target="_blank" rel="noopener">LinkedIn</a>
    · <a href="{{ '/contact/' | relative_url }}">Full contact page</a>
  </p>
</section>
