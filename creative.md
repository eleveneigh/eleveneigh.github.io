---
layout: page
title: Creative
permalink: /creative/
---

<div class="creative-page">
Beyond research, I explore creativity through various mediums that inform my understanding of human expression and design.

<h2>Poetry</h2>

{% assign poems = site.data.creative.poems %}
{% if poems and poems.size > 0 %}
  <div class="creative-list">
    {% for poem in poems %}
    <article class="creative-item">
      <h3>{{ poem.title }}</h3>
      <p>{{ poem.description }}</p>
      <div class="zine-meta">{{ poem.year }} • {{ poem.category }}</div>
      <p class="creative-link-wrap">
        <a href="{{ poem.file | relative_url }}" target="_blank" rel="noopener">Open work (PDF)</a>
      </p>
    </article>
    {% endfor %}
  </div>
{% else %}
  <div class="zine-placeholder">
    <h4>📝 Poetry</h4>
    <p>Add your poetry projects here</p>
  </div>
{% endif %}

<!-- Updated with original PDF images -->
<h2>Zines</h2>

{% assign zines = site.data.creative.zines %}
{% if zines.size > 0 %}
  <div class="creative-list">
  {% for zine in zines %}
  <article class="creative-item">
    <h3>{{ zine.title }}</h3>
    <p>{{ zine.description }}</p>
    <div class="zine-meta">{{ zine.year }} • {{ zine.category }}</div>
    <p class="creative-link-wrap">
      <a href="{{ zine.pdf | relative_url }}" target="_blank" rel="noopener">Open work (PDF)</a>
    </p>
  </article>
  {% endfor %}
  </div>
{% else %}
  <div class="zine-placeholder">
    <h4>📚 Zines</h4>
    <p>Add your zine projects here</p>
  </div>
{% endif %}
</div>

<style>
{% include_relative assets/css/creative.css %}
</style>
