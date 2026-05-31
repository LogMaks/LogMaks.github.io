---
layout: default
title: Portfolio
permalink: /portfolio/
---

<h1>Portfolio</h1>
<p class="lead muted">
  Applied research prototypes and engineering work. Items are experimental or under active development unless a publication or demo link is listed.
</p>

{% assign dst_project = site.projects | where_exp: "item", "item.title contains 'Dempster'" | first %}

<article class="portfolio-card portfolio-anchor" id="dst-diagnostics">
  <h2>Dempster–Shafer Theory for Industrial Diagnostics</h2>
  <p class="portfolio-role"><strong>Role:</strong> Research prototype / published research support</p>
  <p class="keywords">Dempster–Shafer Theory · Belief Functions · Uncertainty Modeling · Industrial Diagnostics · Continuous Casting (CCM)</p>

  <dl class="detail-list">
    <dt>Context</dt>
    <dd>Industrial diagnostics under uncertainty, incomplete observations, and conflicting evidence — focused on continuous casting machines in metallurgy.</dd>
    <dt>Problem</dt>
    <dd>Classical probabilistic models may be brittle when evidence is sparse, imprecise, or conflicting across temperature, vibration, and acoustic sensors.</dd>
    <dt>Approach</dt>
    <dd>Use Dempster–Shafer belief functions to represent uncertainty and combine evidence from diagnostic sources; adaptive combination rules (Dempster / Yager) depending on conflict coefficient.</dd>
    <dt>Evidence</dt>
    <dd>
      <ul class="evidence-list">
        {% if dst_project and dst_project.links.pdf %}
        <li>Peer-reviewed article: <a href="{{ dst_project.links.pdf }}" target="_blank" rel="noopener">VIVT Journal (PDF)</a></li>
        {% elsif dst_project and dst_project.links.article %}
        <li>Peer-reviewed article: <a href="{{ dst_project.links.article }}" target="_blank" rel="noopener">VIVT Journal (PDF)</a></li>
        {% endif %}
        {% if dst_project and dst_project.links.demo %}
        <li>Demo: <a href="{{ dst_project.links.demo }}" target="_blank" rel="noopener">damshaf.onrender.com</a></li>
        {% endif %}
        {% if dst_project %}
        <li>Project page: <a href="{{ dst_project.url | relative_url }}">Dempster–Shafer diagnostics overview</a></li>
        {% endif %}
        <li>Repository: not publicly linked yet</li>
      </ul>
    </dd>
    <dt>Outcome</dt>
    <dd>Experimental validation on CCM diagnostic scenarios reported in the published work: improved diagnostic accuracy and reduced false confidence under high-conflict evidence (see project page for details).</dd>
    <dt>Status</dt>
    <dd>Published research support with working diagnostic prototype demo.</dd>
  </dl>
</article>

{% assign hrl_track = site.projects | where_exp: "item", "item.title contains 'Industrial MRO'" | first %}
{% assign mro_post = site.posts | where_exp: "item", "item.title contains 'Final vision'" | first %}

<article class="portfolio-card" id="mro-marl">
  <h2>Industrial MRO Optimization with Hierarchical MARL</h2>
  <p class="portfolio-role"><strong>Role:</strong> Simulation-based research prototype</p>
  <p class="keywords">Reinforcement Learning · MARL · HRL · CMDP · HITL · Industrial Maintenance · Simulation</p>

  <dl class="detail-list">
    <dt>Context</dt>
    <dd>Industrial maintenance planning under limited maintenance resources and equipment degradation.</dd>
    <dt>Problem</dt>
    <dd>Reactive or fixed-schedule maintenance policies may lead to avoidable downtime or inefficient resource use under stochastic failures and partial observability.</dd>
    <dt>Approach</dt>
    <dd>Simulation-based decision-support prototype using hierarchical RL / MARL, HITL operator feedback, constrained decision-making (CMDP / action masking), and latency-aware intervention logic at the strategic level.</dd>
    <dt>Evidence</dt>
    <dd>
      <ul class="evidence-list">
        {% if hrl_track %}<li>Project page: <a href="{{ hrl_track.url | relative_url }}">PhD research track overview</a></li>{% endif %}
        {% if mro_post %}<li>Working paper draft: <a href="{{ mro_post.url | relative_url }}">Hierarchical MARL framework for MRO</a></li>{% endif %}
        <li>Repository: not publicly linked yet</li>
        <li>Demo / screenshots: to be added</li>
      </ul>
    </dd>
    <dt>Outcome</dt>
    <dd>Simulation experiments compare learned maintenance policies against baseline strategies such as reactive or schedule-based maintenance. Reported trends include a shift toward more preventive planning under resource limits (see working paper draft; no production deployment).</dd>
    <dt>Status</dt>
    <dd>Active research prototype — under development.</dd>
  </dl>
</article>

<article class="portfolio-card" id="rl-envs">
  <h2>RL Simulation Environments</h2>
  <p class="portfolio-role"><strong>Role:</strong> Experimental environment</p>
  <p class="keywords">Python · Gymnasium · PyGame · Simulation · RL Environments · Experiment Logging</p>

  <dl class="detail-list">
    <dt>Context</dt>
    <dd>Reproducible testbeds for hierarchical and multi-agent RL beyond toy benchmarks.</dd>
    <dt>Problem</dt>
    <dd>Maintenance and resource-allocation experiments need configurable simulation environments with logging hooks.</dd>
    <dt>Approach</dt>
    <dd>Custom Gymnasium-style environments modeling equipment fleet dynamics, maintenance actions, and resource constraints.</dd>
    <dt>Evidence</dt>
    <dd>
      <ul class="evidence-list">
        <li>Repository: not publicly linked yet</li>
      </ul>
    </dd>
    <dt>Status</dt>
    <dd>Experimental environment — iterative development.</dd>
  </dl>
</article>

<article class="portfolio-card" id="mlops-sandbox">
  <h2>Data / ML Engineering Sandbox</h2>
  <p class="portfolio-role"><strong>Role:</strong> Engineering sandbox (under development)</p>
  <p class="keywords">Python · SQL · FastAPI · Docker · Experiment Tracking</p>

  <dl class="detail-list">
    <dt>Context</dt>
    <dd>Small research-oriented prototypes: data-processing scripts, API experiments, and reproducible experiment pipelines.</dd>
    <dt>Problem</dt>
    <dd>Bridging research experiments with lightweight data workflows and serving stubs.</dd>
    <dt>Approach</dt>
    <dd>Python / SQL-based data and ML prototypes; containerized API experiments; tracked experiment runs.</dd>
    <dt>Evidence</dt>
    <dd>
      <ul class="evidence-list">
        <li>Repository: not publicly linked yet</li>
      </ul>
    </dd>
    <dt>Status</dt>
    <dd>Under development — no public artifact yet.</dd>
  </dl>
</article>
