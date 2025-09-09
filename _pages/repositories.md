---
layout: page
permalink: /repositories/
title: Repositories
description:
nav: true
nav_order: 3
---

[GAUCHE](https://slideslive.com/39008487/gauche-a-library-for-gaussian-processes-in-chemistry) is a software library that extends the Gaussian process framework to operate on molecular representations such as Morgan fingerprints, SMILES strings, and graphs. The most common industrials use-case for GAUCHE has been to support active learning and Bayesian optimization loops with Gaussian process surrogate models. Here's a [tutorial](https://github.com/leojklarner/gauche/blob/main/notebooks/GP%20Regression%20on%20Molecules.ipynb). [Aviary](https://arxiv.org/abs/2412.21154) and its sister library [LDP](https://github.com/Future-House/ldp) are software libraries for implementing language agents and environments. Here's a [tutorial](https://github.com/Future-House/aviary/blob/main/tutorials/Building%20a%20Custom%20Environment%20in%20Aviary.ipynb).

{% if site.data.repositories.github_users %}

## GitHub users

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>

---

{% if site.repo_trophies.enabled %}
{% for user in site.data.repositories.github_users %}
{% if site.data.repositories.github_users.size > 1 %}

  <h4>{{ user }}</h4>
  {% endif %}
  <div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo_trophies.liquid username=user %}
  </div>

---

{% endfor %}
{% endif %}
{% endif %}

{% if site.data.repositories.github_repos %}

## GitHub Repositories

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}
