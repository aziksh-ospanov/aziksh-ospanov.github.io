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

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-start">
  {% for repo in site.data.repositories.github_repos %}
    <div class="mb-4 me-md-3" style="max-width: 260px;">
      <a href="{{ repo.url }}"
         target="_blank"
         rel="noopener noreferrer"
         style="text-decoration: none;">
        <img
          src="{{ repo.image | relative_url }}"
          alt="{{ repo.name }} image"
          class="img-fluid mb-2"
          style="border-radius: 0.5rem;">
        <div class="fw-semibold">
          {{ repo.name }}
        </div>
      </a>
    </div>
  {% endfor %}
</div>
{% endif %}
