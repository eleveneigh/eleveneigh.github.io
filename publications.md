---
layout: page
title: Publications
permalink: /publications/
---

{% assign pubs = site.data.publications %}

<div class="publications-page">
  <p class="publications-intro">
    Selected publications and manuscripts. For collaboration inquiries, see
    <a href="{{ '/contact/' | relative_url }}">Contact</a>.
  </p>

  {% if pubs and pubs.size > 0 %}
  <div class="publications-list">
    {% for pub in pubs %}
    <article class="publication-item">
      <h2 class="publication-title">{{ pub.title }}</h2>
      <p class="publication-authors">{{ pub.authors }}</p>
      <p class="publication-venue">{{ pub.venue }} · {{ pub.year }}</p>
      <p class="publication-meta">
        <span class="publication-role">{{ pub.role }}</span>
        <span class="publication-status">{{ pub.status }}</span>
      </p>
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
