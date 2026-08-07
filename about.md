---
layout: page
title: About
permalink: /about/
body_class: about-page
---

{% assign profile = site.data.profile %}

<div class="about-editorial">
  <p class="about-lede">{{ profile.identity }}</p>

  <section class="about-section about-vision" aria-labelledby="about-vision-title">
    <p class="editorial-index">01 / RESEARCH VISION</p>
    <h2 id="about-vision-title">Designing space for reflection.</h2>
    <p class="about-vision-statement">{{ profile.vision }}</p>
    <p>{{ profile.vision_note }} → <a href="{{ '/creative/' | relative_url }}">See Practice</a> for some of that earlier work.</p>
  </section>

  <div class="about-two-column">
    <section class="about-section" aria-labelledby="about-interests-title">
      <p class="editorial-index">02 / INTERESTS</p>
      <h2 id="about-interests-title">Questions I return to</h2>
      <ol class="numbered-notes">
        {% for item in profile.interests %}<li>{{ item }}</li>{% endfor %}
      </ol>
    </section>

    <section class="about-section" aria-labelledby="about-methods-title">
      <p class="editorial-index">03 / METHODS</p>
      <h2 id="about-methods-title">How I work</h2>
      <ol class="numbered-notes">
        {% for item in profile.methods %}<li>{{ item }}</li>{% endfor %}
      </ol>
    </section>
  </div>

  <section class="about-section about-goals" aria-labelledby="about-goals-title">
    <p class="editorial-index">04 / NEXT</p>
    <h2 id="about-goals-title">Where this work is going</h2>
    <p>{{ profile.looking_for }} <a href="mailto:lw403@duke.edu">Get in touch →</a></p>
    {% if profile.cv and profile.cv != "" %}<p><a href="{{ profile.cv | relative_url }}">Download CV (PDF)</a></p>{% endif %}
  </section>

  <aside class="about-aside">
    <div>
      <p class="editorial-index">MARGINALIA / WOLFGANG</p>
      <p class="about-aside-text">{{ profile.wolfgang }}</p>
    </div>
    <img
      class="about-aside-photo"
      src="{{ profile.wolfgang_photo | relative_url }}"
      alt="Wolfgang"
      width="800"
      height="600"
      loading="lazy"
    >
  </aside>
</div>
