---
layout: page
permalink: /people/
title: People
nav: true
nav_order: 1
---

<div class="people">
<hr>
{% for person in site.data.people %}
  <div class="row align-items-center my-5">
    {% assign is_even = forloop.index | modulo: 2 %}
    {% if is_even == 0 %}
    <div class="col-sm-4 text-center">
      <img src="{{ person.image | prepend: '/assets/img/' | relative_url }}" alt="{{ person.name }}" class="img-fluid rounded z-depth-1" style="max-height: 300px; width: auto;">
    </div>
    <div class="col-sm-8">
      <h3 class="mb-1">{{ person.name }}</h3>
      {% if person.position %}<p class="text-muted mb-2"><strong>{{ person.position }}</strong></p>{% endif %}
      {% if person.bio %}<p>{{ person.bio }}</p>{% endif %}
      {% if person.linkedin %}<a href="{{ person.linkedin }}" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn"><i class="fa-brands fa-linkedin fa-lg"></i></a>{% endif %}
    </div>
    {% else %}
    <div class="col-sm-8">
      <h3 class="mb-1">{{ person.name }}</h3>
      {% if person.position %}<p class="text-muted mb-2"><strong>{{ person.position }}</strong></p>{% endif %}
      {% if person.bio %}<p>{{ person.bio }}</p>{% endif %}
      {% if person.linkedin %}<a href="{{ person.linkedin }}" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn"><i class="fa-brands fa-linkedin fa-lg"></i></a>{% endif %}
    </div>
    <div class="col-sm-4 text-center">
      <img src="{{ person.image | prepend: '/assets/img/' | relative_url }}" alt="{{ person.name }}" class="img-fluid rounded z-depth-1" style="max-height: 300px; width: auto;">
    </div>
    {% endif %}
  </div>
  {% unless forloop.last %}<hr>{% endunless %}
{% endfor %}
</div>
