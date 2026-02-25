---
permalink: /research/
title: "Research"
layout: single
author_profile: true
---

My work focuses on building and validating geospatial AI systems that turn large environmental datasets into decision-ready insights—for carbon accounting, biodiversity monitoring, and ecosystem service quantification.

<div class="research-grid">
  {% assign projects = site.research | sort: 'order' %}
  {% for project in projects %}
  <a href="{{ project.url | relative_url }}" class="research-card">
    {% if project.hero_image %}
      <img class="research-card__image" src="{{ project.hero_image | relative_url }}" alt="{{ project.title }}">
    {% else %}
      <div class="research-card__placeholder">🌿</div>
    {% endif %}
    <div class="research-card__body">
      <div class="research-card__title">{{ project.title }}</div>
      <p class="research-card__excerpt">{{ project.excerpt }}</p>
      {% if project.tags %}
      <div class="research-card__tags">
        {% for tag in project.tags limit:4 %}
        <span class="research-card__tag">{{ tag }}</span>
        {% endfor %}
      </div>
      {% endif %}
    </div>
  </a>
  {% endfor %}
</div>
