---
layout: page
permalink: /media/
title: Media
nav: true
nav_order: 4
---

<div class="row">
{% for item in site.data.media %}
  <div class="col-md-6 mb-4">
    <div class="card h-100">
      <a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">
        <img src="{{ item.thumbnail }}"
             alt="{{ item.title }}"
             class="card-img-top"
             style="object-fit: contain; height: 200px; width: 100%; background-color: #00818A;">
      </a>
      <div class="card-body">
        <h5 class="card-title">{{ item.title }}</h5>
        <p class="card-text text-muted">{{ item.subtitle }}</p>
      </div>
    </div>
  </div>
{% endfor %}
</div>
