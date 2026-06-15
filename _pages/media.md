---
layout: page
permalink: /media/
title: media
nav: true
nav_order: 4
---

<div class="row">
{% for item in site.data.media %}
  <div class="col-md-6 mb-4">
    <div class="card h-100">
      <a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">
        <img src="{{ item.thumbnail | prepend: '/assets/img/' | relative_url }}"
             alt="{{ item.title }}"
             class="card-img-top"
             style="object-fit: cover; height: 200px; width: 100%;">
      </a>
      <div class="card-body">
        <h5 class="card-title">{{ item.title }}</h5>
        <p class="card-text text-muted">{{ item.subtitle }}</p>
      </div>
    </div>
  </div>
{% endfor %}
</div>
