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

<style>
.projects-page {
  max-width: 960px;
  margin: 0 auto;
}

.projects-grid {
  display: grid;
  gap: 1.25rem;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
}

.project-card {
  border: 1px solid var(--border, #e2e8f0);
  background: var(--bg-card, #fff);
  padding: 1.25rem;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
}

.project-title {
  margin: 0;
  font-size: 1.25rem;
}

.project-role,
.project-period,
.project-brief,
.project-paper {
  margin: 0;
}

.project-role {
  color: var(--text-primary, #2d3748);
  font-weight: 500;
}

.project-period {
  color: var(--text-accent, #4a5568);
  font-size: 0.95rem;
}

.project-brief {
  color: var(--text-secondary, #718096);
}

.project-highlights {
  margin: 0;
  padding-left: 1.1rem;
  color: var(--text-secondary, #718096);
}

.project-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.45rem;
}

.project-tag {
  border: 1px solid var(--border, #e2e8f0);
  border-radius: 999px;
  padding: 0.2rem 0.55rem;
  font-size: 0.82rem;
  color: var(--text-accent, #4a5568);
}
</style>
