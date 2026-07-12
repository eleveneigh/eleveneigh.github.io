---
layout: page
title: Publications
permalink: /publications/
---

{% assign pubs = site.data.publications %}

<div class="publications-page">
  {% if pubs and pubs.size > 0 %}
  <div class="publications-list">
    {% for pub in pubs %}
    <article class="publication-item">
      <h2 class="publication-title">
        {% if pub.link and pub.link != "" %}
        <a href="{{ pub.link }}" target="_blank" rel="noopener noreferrer">{{ pub.title }}</a>
        {% else %}
        {{ pub.title }}
        {% endif %}
      </h2>
      <p class="publication-authors">{{ pub.authors }} ({{ pub.role }})</p>
      <p class="publication-venue">{{ pub.venue }} · {{ pub.status }}</p>
      {% if pub.link and pub.link != "" %}
      <p><a href="{{ pub.link }}" target="_blank" rel="noopener noreferrer">View paper →</a></p>
      {% endif %}
    </article>
    {% endfor %}
  </div>
  {% else %}
  <p>No publications listed yet.</p>
  {% endif %}
</div>
