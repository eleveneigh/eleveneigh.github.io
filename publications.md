---
layout: page
title: Publications
permalink: /publications/
body_class: publications-page
---

{% assign pubs = site.data.publications %}

<div class="publications-page-inner">
  <div class="publications-intro-grid">
    <p class="editorial-index">WRITING / PROCEEDINGS</p>
    <p>Selected publications across human–AI collaboration, creative systems, and reflective making.</p>
  </div>
  {% if pubs and pubs.size > 0 %}
  <div class="publications-list">
    {% for pub in pubs %}
    <article class="publication-item">
      <span class="publication-number">0{{ forloop.index }}</span>
      <div class="publication-copy">
        <p class="publication-venue">{{ pub.venue }} · {{ pub.status }}</p>
        <h2 class="publication-title">{{ pub.title }}</h2>
        <p class="publication-authors">{{ pub.authors }} <span>({{ pub.role }})</span></p>
        {% if pub.link and pub.link != "" %}
        <p><a class="text-arrow" href="{{ pub.link }}" target="_blank" rel="noopener noreferrer">View paper <span>↗</span></a></p>
        {% endif %}
      </div>
    </article>
    {% endfor %}
  </div>
  {% else %}
  <p>No publications listed yet.</p>
  {% endif %}
</div>
