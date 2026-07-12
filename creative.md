---
layout: page
title: Practice
permalink: /creative/
---

<div class="creative-page">
<p class="practice-framing">{{ site.data.creative.framing }}</p>

<h2>Film</h2>

{% assign films = site.data.creative.films %}
{% if films and films.size > 0 %}
  <div class="creative-list">
    {% for film in films %}
    <article class="creative-item film-entry">
      <h3>{{ film.title }}</h3>
      <div class="zine-meta">{{ film.role }}</div>
      <div class="zine-meta">{{ film.place }} · {{ film.period }}</div>

      {% if film.photos and film.photos.size > 0 %}
      <div class="film-photo-grid" aria-label="Behind-the-scenes stills">
        {% for photo in film.photos %}
        <img src="{{ photo | relative_url }}" alt="Still from {{ film.title }}" loading="lazy">
        {% endfor %}
      </div>
      {% endif %}

      <p>{{ film.synopsis }}</p>
      <p>{{ film.process }}</p>
      {% if film.status %}
      <p class="film-status">{{ film.status }}</p>
      {% endif %}

      {% if film.script and film.script != "" %}
      <p class="creative-link-wrap">
        <a href="{{ film.script | relative_url }}" target="_blank" rel="noopener noreferrer">Click to view the script</a>
      </p>
      {% endif %}
    </article>
    {% endfor %}
  </div>
{% endif %}

<h2>Poetry</h2>

{% assign poems = site.data.creative.poems %}
{% if poems and poems.size > 0 %}
  <div class="creative-list">
    {% for poem in poems %}
    <article class="creative-item">
      <h3>{{ poem.title }}</h3>
      <p>{{ poem.description }}</p>
      <div class="zine-meta">{{ poem.year }} • {{ poem.category }}</div>
      {% if poem.research_note %}
      <p class="creative-research-note">{{ poem.research_note }}</p>
      {% endif %}
      <p class="creative-link-wrap">
        <a href="{{ poem.file | relative_url }}" target="_blank" rel="noopener noreferrer">Open work (PDF)</a>
      </p>
    </article>
    {% endfor %}
  </div>
{% else %}
  <div class="zine-placeholder">
    <h4>Poetry</h4>
    <p>Add your poetry projects in <code>_data/creative.yml</code>.</p>
  </div>
{% endif %}

<h2>Zines</h2>

{% assign zines = site.data.creative.zines %}
{% if zines.size > 0 %}
  <div class="creative-list">
  {% for zine in zines %}
  <article class="creative-item">
    <h3>{{ zine.title }}</h3>
    <p>{{ zine.description }}</p>
    <div class="zine-meta">{{ zine.year }} • {{ zine.category }}</div>
    {% if zine.research_note %}
    <p class="creative-research-note">{{ zine.research_note }}</p>
    {% endif %}
    <p class="creative-link-wrap">
      <a href="{{ zine.pdf | relative_url }}" target="_blank" rel="noopener noreferrer">Open work (PDF)</a>
    </p>
  </article>
  {% endfor %}
  </div>
{% else %}
  <div class="zine-placeholder">
    <h4>Zines</h4>
    <p>Add zine entries in <code>_data/creative.yml</code>.</p>
  </div>
{% endif %}
</div>
