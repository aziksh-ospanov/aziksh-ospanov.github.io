---
layout: page
permalink: /repositories/
title: repositories
description: Edit the `_data/repositories.yml` and change the `github_users` and `github_repos` lists to include your own GitHub profile and repositories.
nav: true
nav_order: 4
---

{% if site.data.repositories.github_repos %}

## GitHub Repositories

{% if site.data.repositories.github_repos %}

## GitHub Repositories

<div class="repositories d-flex flex-wrap flex-md-row flex-column gap-4">
  {% for repo in site.data.repositories.github_repos %}
    <div class="repo-card">
      <a href="{{ repo.url }}" target="_blank" rel="noopener noreferrer">
        
        <div class="repo-image-wrapper">
          <img src="{{ repo.image | relative_url }}" alt="{{ repo.name }}">
        </div>

        <div class="repo-title">
          {{ repo.name }}
        </div>

      </a>
    </div>
  {% endfor %}
</div>

{% endif %}

