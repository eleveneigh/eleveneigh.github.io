---
layout: page
title: Research
permalink: /projects/
---

{% assign projects = site.data.projects %}
{% assign theme_co = "Co-Creative Systems" %}
{% assign theme_well = "AI & Well-being" %}

<div class="projects-page">
  <p class="projects-intro">
    Research organized by theme. Each project includes motivation, contribution, insights, and reflection.
  </p>

  {% if projects.size > 0 %}
    <section class="project-theme-group">
      <h2>{{ theme_co }}</h2>
      <div class="projects-grid">
        {% for p in projects %}
          {% if p.theme == theme_co %}
          <article class="project-card">
            <h3 class="project-title">
              <a href="{{ '/research/' | append: p.slug | append: '/' | relative_url }}">{{ p.name }}</a>
            </h3>
            {% if p.period %}<p class="project-period">{{ p.period }}</p>{% endif %}
            {% if p.brief %}<p class="project-brief">{{ p.brief }}</p>{% endif %}
            {% if p.insight %}
            <p class="project-insight"><strong>Insight:</strong> {{ p.insight }}</p>
            {% endif %}
            <p class="project-card-link-wrap">
              <a href="{{ '/research/' | append: p.slug | append: '/' | relative_url }}">Read case study →</a>
            </p>
          </article>
          {% endif %}
        {% endfor %}
      </div>
    </section>

    <section class="project-theme-group">
      <h2>{{ theme_well }}</h2>
      <div class="projects-grid">
        {% for p in projects %}
          {% if p.theme == theme_well %}
          <article class="project-card">
            <h3 class="project-title">
              <a href="{{ '/research/' | append: p.slug | append: '/' | relative_url }}">{{ p.name }}</a>
            </h3>
            {% if p.period %}<p class="project-period">{{ p.period }}</p>{% endif %}
            {% if p.brief %}<p class="project-brief">{{ p.brief }}</p>{% endif %}
            {% if p.insight %}
            <p class="project-insight"><strong>Insight:</strong> {{ p.insight }}</p>
            {% endif %}
            <p class="project-card-link-wrap">
              <a href="{{ '/research/' | append: p.slug | append: '/' | relative_url }}">Read case study →</a>
            </p>
          </article>
          {% endif %}
        {% endfor %}
      </div>
    </section>
  {% else %}
    <p>No projects yet. Add entries in <code>_data/projects.yml</code>.</p>
  {% endif %}
</div>
