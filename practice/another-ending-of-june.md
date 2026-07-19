---
layout: page
title: Another Ending of June
permalink: /practice/another-ending-of-june/
---

{% assign film = site.data.creative.films | where: "slug", "another-ending-of-june" | first %}

<div class="film-detail">
  <p class="film-detail-meta">{{ film.role }}</p>
  <p class="film-detail-meta">{{ film.place }} · {{ film.period }}</p>

  <p>{{ film.synopsis }}</p>
  <p>{{ film.process }}</p>
  {% if film.status %}
  <p class="film-status">{{ film.status }}</p>
  {% endif %}

  <h2>Stills</h2>
  <div class="film-photo-grid film-photo-grid-full" aria-label="Behind-the-scenes stills">
    {% for photo in film.photos %}
    <img src="{{ photo | relative_url }}" alt="Still from {{ film.title }}" loading="lazy">
    {% endfor %}
  </div>

  <h2>Script</h2>
  {% include scripts/another-ending-of-june.html %}

  <p class="case-study-back">
    <a href="{{ '/creative/' | relative_url }}">← Back to Practice</a>
  </p>
</div>
