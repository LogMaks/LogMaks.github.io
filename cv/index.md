---
layout: default
title: CV
permalink: /cv/
---

<h1>CV</h1>

<h2>Profile</h2>
<p>
  AI / ML researcher and developer focused on reinforcement learning, multi-agent systems,
  and simulation-based industrial decision-support prototypes.
</p>

<h2>Target Roles</h2>
<ul>
  <li>ML Engineer</li>
  <li>Data Engineer</li>
  <li>ML / RL Researcher</li>
  <li>Research Engineer</li>
  <li>Industrial AI / Decision Support Prototyping</li>
</ul>

<h2>Education</h2>
<ul>
  <li>Master's degree — details to be added</li>
  <li>PhD (Candidate) research track — formal models for hierarchical MARL in industrial MRO — institution and timeline to be added</li>
</ul>

<h2>Research Interests</h2>
<ul>
  <li>Reinforcement Learning</li>
  <li>Multi-Agent Systems</li>
  <li>Hierarchical RL</li>
  <li>Human-in-the-Loop decision-making</li>
  <li>Dempster–Shafer theory</li>
  <li>Industrial maintenance optimization</li>
</ul>

<h2>Technical Skills</h2>

<h3>Machine Learning / RL</h3>
<ul>
  <li>Reinforcement Learning</li>
  <li>Multi-Agent Reinforcement Learning</li>
  <li>Hierarchical RL</li>
  <li>Simulation-based optimization</li>
  <li>Experiment logging</li>
</ul>

<h3>Data / Engineering</h3>
<ul>
  <li>Python</li>
  <li>C++</li>
  <li>SQL</li>
  <li>Data analysis</li>
  <li>API prototypes</li>
  <li>Docker</li>
  <li>Linux</li>
  <li>Git</li>
</ul>

<h3>Tools</h3>
<p class="muted">Listed only where referenced in site projects and posts:</p>
<ul>
  <li>Gymnasium (simulation environments)</li>
  <li>PyGame (visualization)</li>
  <li>FastAPI (API prototypes)</li>
  <li>Docker (containerized experiments)</li>
</ul>

<h2>Selected Projects</h2>
<ul>
  <li><a href="{{ '/portfolio/#dst-diagnostics' | relative_url }}">Dempster–Shafer Theory for Industrial Diagnostics</a> — published research + demo</li>
  <li><a href="{{ '/portfolio/#mro-marl' | relative_url }}">Industrial MRO Optimization with Hierarchical MARL</a> — simulation research prototype</li>
  <li><a href="{{ '/portfolio/#rl-envs' | relative_url }}">RL Simulation Environments</a> — experimental testbeds</li>
  <li><a href="{{ '/portfolio/#mlops-sandbox' | relative_url }}">Data / ML Engineering Sandbox</a> — under development</li>
</ul>

<h2>Publications / Research Outputs</h2>
<p>Peer-reviewed publications, accepted manuscripts, working papers, and concept notes are maintained on the <a href="{{ '/research/' | relative_url }}">Research</a> page.</p>
<ul>
  <li><a href="{{ '/research/' | relative_url }}#track-a1">Research directions &amp; publication table</a></li>
  {% assign dst = site.projects | where_exp: "p", "p.title contains 'Dempster'" | first %}
  {% if dst %}<li><a href="{{ dst.url | relative_url }}">{{ dst.title }}</a> — Published</li>{% endif %}
</ul>

<h2>Contact</h2>
<ul class="contact-links">
  <li><a href="https://github.com/LogMaks" target="_blank" rel="noopener">GitHub — LogMaks</a></li>
  <li><a href="https://www.linkedin.com/in/lomaxart/" target="_blank" rel="noopener">LinkedIn</a></li>
  <li><a href="https://scholar.google.com/citations?user=YDrAHzgAAAAJ" target="_blank" rel="noopener">Google Scholar</a></li>
  <li><a href="https://orcid.org/my-orcid?orcid=0009-0005-7256-5718" target="_blank" rel="noopener">ORCID</a></li>
  <li><a href="mailto:lomaxart@gmail.com">lomaxart@gmail.com</a></li>
</ul>

<p class="muted">
  PDF version: <a href="{{ '/assets/cv_en.pdf' | relative_url }}" target="_blank" rel="noopener">Download CV (PDF)</a>
</p>
