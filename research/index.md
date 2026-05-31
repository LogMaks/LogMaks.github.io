---
layout: default
title: Research
permalink: /research/
---

<h1>Research</h1>

<p class="lead">
  Decision-making systems under uncertainty — reinforcement learning, multi-agent coordination,
  human-in-the-loop control, and industrial maintenance optimization.
  Peer-reviewed publications, manuscripts in progress, and concept notes are listed separately below.
</p>

<h2>Peer-reviewed / Published</h2>
<div class="table-wrap">
<table class="research-table">
  <thead>
    <tr>
      <th>Title</th>
      <th>Status</th>
      <th>Venue</th>
      <th>Year</th>
      <th>Links</th>
    </tr>
  </thead>
  <tbody>
    {% for item in site.data.research_outputs.peer_reviewed %}
    <tr>
      <td>{{ item.title }}</td>
      <td><span class="status-badge">{{ item.status }}</span></td>
      <td>{{ item.venue | default: "TBD" }}</td>
      <td>{{ item.year | default: "TBD" }}</td>
      <td class="links-cell">
        {% for link in item.links %}
          <a href="{{ link.url }}" target="_blank" rel="noopener">{{ link.label }}</a>{% unless forloop.last %} · {% endunless %}
        {% endfor %}
        {% if item.project_match %}
          {% assign proj = site.projects | where_exp: "p", "p.title contains item.project_match" | first %}
          {% if proj %} · <a href="{{ proj.url | relative_url }}">Project page</a>{% endif %}
        {% endif %}
      </td>
    </tr>
    {% endfor %}
    {% for item in site.data.research_outputs.accepted %}
    <tr>
      <td>{{ item.title }}</td>
      <td><span class="status-badge">{{ item.status }}</span></td>
      <td>{{ item.venue | default: "TBD" }}</td>
      <td>{{ item.year | default: "TBD" }}</td>
      <td class="links-cell">
        {% for link in item.links %}
          <a href="{{ link.url }}" target="_blank" rel="noopener">{{ link.label }}</a>{% unless forloop.last %} · {% endunless %}
        {% endfor %}
      </td>
    </tr>
    {% endfor %}
  </tbody>
</table>
</div>

<h2>Manuscripts in Progress</h2>
<div class="table-wrap">
<table class="research-table">
  <thead>
    <tr>
      <th>Title</th>
      <th>Status</th>
      <th>Venue</th>
      <th>Year</th>
      <th>Links</th>
    </tr>
  </thead>
  <tbody>
    {% for item in site.data.research_outputs.manuscripts %}
    <tr>
      <td>{{ item.title }}</td>
      <td><span class="status-badge">{{ item.status }}</span></td>
      <td>{{ item.venue | default: "TBD" }}</td>
      <td>{{ item.year | default: "TBD" }}</td>
      <td class="links-cell">
        {% if item.post_match %}
          {% assign note = site.posts | where_exp: "p", "p.title contains item.post_match" | first %}
          {% if note %}<a href="{{ note.url | relative_url }}">Draft / note</a>{% else %}TBD{% endif %}
        {% else %}TBD{% endif %}
      </td>
    </tr>
    {% endfor %}
  </tbody>
</table>
</div>

<h2>Research Directions</h2>
<p class="muted">Active research tracks — not yet standalone publications.</p>
{% for item in site.data.research_outputs.research_directions %}
<article class="track-card" id="{{ item.id }}">
  <h3>{{ item.title }}</h3>
  <p><strong>Focus:</strong> {{ item.focus }}</p>
  <p class="track-links">
    {% if item.project_match %}
      {% assign proj = site.projects | where_exp: "p", "p.title contains item.project_match" | first %}
      {% if proj %}<a href="{{ proj.url | relative_url }}">Project overview</a>{% endif %}
    {% endif %}
    {% if item.post_match %}
      {% assign note = site.posts | where_exp: "p", "p.title contains item.post_match" | first %}
      {% if note %}{% if item.project_match %} · {% endif %}<a href="{{ note.url | relative_url }}">Related note</a>{% endif %}
    {% endif %}
  </p>
</article>
{% endfor %}

<h2>Collaborations / Side Research</h2>
<ul class="collab-list">
  {% for item in site.data.research_outputs.collaborations %}
  <li>
    <strong>{{ item.title }}</strong> — {{ item.status }}.
    {{ item.note }}
    {% if item.project_match %}
      {% assign proj = site.projects | where_exp: "p", "p.title contains item.project_match" | first %}
      {% if proj %}<a href="{{ proj.url | relative_url }}">Details</a>{% endif %}
    {% endif %}
  </li>
  {% endfor %}
  {% assign gestalt = site.projects | where_exp: "p", "p.title contains 'Gestalt'" | first %}
  {% if gestalt %}
  <li>
    <strong>{{ gestalt.title }}</strong> — Concept note.
    Research direction on resource coordination in multi-agent systems.
    <a href="{{ gestalt.url | relative_url }}">Details</a>
  </li>
  {% endif %}
</ul>

<h2>Talks</h2>
<p class="muted">No public talk recordings listed yet. <a href="{{ '/contact/' | relative_url }}">Contact me</a> for seminar or conference materials upon request.</p>

<h2>Open Research Questions</h2>
<ul>
  <li>How to formalize operator uncertainty and approval latency in hierarchical HITL-RL without breaking policy improvement guarantees?</li>
  <li>Can evidential (DST) belief updates be integrated into constrained MDP decision layers for interpretable maintenance diagnostics?</li>
  <li>What resource-allocation mechanisms best support leadership migration in marginal hierarchical multi-agent control?</li>
  <li>How to evaluate simulation-based maintenance policies under distributional shift between synthetic environments and operational data?</li>
</ul>

<p class="section-link"><a href="{{ '/projects/' | relative_url }}">Legacy projects index →</a></p>
