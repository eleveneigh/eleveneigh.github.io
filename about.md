---
layout: page
title: About
permalink: /about/
---

{% assign profile = site.data.profile %}

{{ profile.identity }}

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

<p>Open to research collaborations — <a href="mailto:lw403@duke.edu">get in touch</a>.</p>
