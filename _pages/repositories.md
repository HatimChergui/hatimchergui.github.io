---
layout: page
permalink: /repositories/
title: Repositories
nav: true
nav_order: 3
---

{% if site.data.repositories.github_users %}
<h2>GitHub Users</h2>

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>

<hr>

{% if site.repo_trophies and site.repo_trophies.enabled %}
  {% for user in site.data.repositories.github_users %}
    {% if site.data.repositories.github_users.size > 1 %}
      <h4>{{ user }}</h4>
    {% endif %}
    <div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
      {% include repository/repo_trophies.liquid username=user %}
    </div>
    <hr>
  {% endfor %}
{% endif %}
{% endif %}

{% if site.data.repositories.github_repos %}
<h2>GitHub Repositories</h2>

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}

<hr>

<h2>mfoxh-GPU</h2>
<p>
  <a href="https://doi.org/10.5281/zenodo.11316270">
    <img src="https://zenodo.org/badge/DOI/10.5281/zenodo.11316270.svg" alt="DOI Badge">
  </a>
</p>
<p>
  A GPU-enabled Matlab implementation of the multivariate Fox H-function.
  <span style="color:purple;">It can also be used on CPU by dropping <code>gpuArray()</code> function.</span>
</p>
<p>
  <a href="https://zenodo.org/records/11316270">
    <img src="https://api.microlink.io/?url=https%3A%2F%2Fzenodo.org%2Frecords%2F11316270%23metrics&screenshot=true&embed=screenshot.url"
         alt="Zenodo Page" width="600" height="400">
  </a>
</p>

<hr>

<h2>mfoxh-C-MEX</h2>
<p>
  <a href="https://doi.org/10.5281/zenodo.1217925">
    <img src="https://zenodo.org/badge/DOI/10.5281/zenodo.1217925.svg" alt="DOI Badge">
  </a>
</p>
<p>
  A C/MEX parallel multi-thread implementation for the multivariate Fox H-function.
</p>
<p>
  <a href="https://zenodo.org/records/1217925">
    <img src="https://api.microlink.io/?url=https%3A%2F%2Fzenodo.org%2Frecords%2F1217925%23metrics&screenshot=true&embed=screenshot.url"
         alt="Zenodo Page" width="600" height="400">
  </a>
</p>
