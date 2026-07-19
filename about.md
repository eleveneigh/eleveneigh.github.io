---
layout: page
title: About
permalink: /about/
body_class: about-page
---

{% assign profile = site.data.profile %}

<p>{{ profile.identity }}</p>

## Research Vision

<p>{{ profile.vision }}</p>

<p>{{ profile.vision_note }} → <a href="{{ '/creative/' | relative_url }}">See Practice</a> for some of that earlier work.</p>

## Research Interests

{% for item in profile.interests %}
- {{ item }}
{% endfor %}

## Methods

{% for item in profile.methods %}
- {{ item }}
{% endfor %}

## Goals

<p>{{ profile.looking_for }} Open to research collaborations — <a href="mailto:lw403@duke.edu">get in touch</a>.</p>

{% if profile.cv and profile.cv != "" %}
<p><a href="{{ profile.cv | relative_url }}">Download CV (PDF)</a></p>
{% endif %}

<hr class="about-divider">

<div class="about-aside">
  <p class="about-aside-text">{{ profile.wolfgang }}</p>
  <img
    class="about-aside-photo"
    src="{{ profile.wolfgang_photo | relative_url }}"
    alt="Wolfgang"
    width="800"
    height="600"
    loading="lazy"
  >
</div>
