---
layout: page
title: Projects
permalink: /projects/
---

{% assign projects = site.data.projects %}

<div class="projects-page">
  {% if projects.size > 0 %}
    <div class="projects-grid">
      {% for p in projects %}
      <article class="project-card">
        <h2 class="project-title">{{ p.name }}</h2>
        {% if p.role %}<p class="project-role">{{ p.role }}</p>{% endif %}
        {% if p.period %}<p class="project-period">{{ p.period }}</p>{% endif %}

        {% if p.brief %}
        <p class="project-brief">{{ p.brief }}</p>
        {% endif %}

        {% if p.highlights and p.highlights.size > 0 %}
        <ul class="project-highlights">
          {% for item in p.highlights %}
          <li>{{ item }}</li>
          {% endfor %}
        </ul>
        {% endif %}

        {% if p.tags and p.tags.size > 0 %}
        <div class="project-tags">
          {% for tag in p.tags %}
          <span class="project-tag">{{ tag }}</span>
          {% endfor %}
        </div>
        {% endif %}

        {% if p.paper %}
        <p class="project-paper"><strong>Publication:</strong> {{ p.paper }}</p>
        {% endif %}
      </article>
      {% endfor %}
    </div>
  {% else %}
    <p>No projects yet. Add entries in <code>_data/projects.yml</code>.</p>
  {% endif %}
</div>
