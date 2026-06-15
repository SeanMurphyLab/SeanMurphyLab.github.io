---
layout: page
title: Bookshelf
permalink: /books/
nav: false
---

Books authored and edited by the Murphy Lab.

<div class="books mt-4">
{% for book in site.data.books %}
  <div class="row align-items-center mb-5">
    <div class="col-sm-3 mb-3 mb-sm-0 text-center">
      <a href="{{ book.url }}" target="_blank" rel="noopener noreferrer">
        <img src="{{ book.cover | relative_url }}" alt="{{ book.title }} cover"
             style="max-height: 220px; width: auto; max-width: 100%;">
      </a>
    </div>
    <div class="col-sm-9">
      <h3 class="mt-0">
        <a href="{{ book.url }}" target="_blank" rel="noopener noreferrer">{{ book.title }}</a>
      </h3>
      <p class="text-muted mb-2">{{ book.publisher }} · {{ book.year }}</p>
      <p class="mb-0">{{ book.blurb }}</p>
    </div>
  </div>
{% endfor %}
</div>
