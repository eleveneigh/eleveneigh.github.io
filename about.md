---
layout: page
title: About
permalink: /about/
---

{% assign profile = site.data.profile %}

I'm a CS & Applied Mathematics student at Duke Kunshan University, researching at the intersection of **Human-Computer Interaction**, **affective computing**, and **AI-assisted creativity**.

## Research Vision

{{ profile.vision }}

## Research Interests

{% for item in profile.interests %}
- {{ item }}
{% endfor %}

## Methods

{% for item in profile.methods %}
- {{ item }}
{% endfor %}

## Goals

{{ profile.looking_for }}

{% if profile.cv and profile.cv != "" %}
<p><a href="{{ profile.cv | relative_url }}">Download CV (PDF)</a></p>
{% endif %}

<p>Open to research collaborations — <a href="{{ '/contact/' | relative_url }}">get in touch</a>.</p>
