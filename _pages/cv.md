---
layout: academic-page
permalink: /cv/
title: "Curriculum Vitae"
eyebrow: "Profile"
intro: "A concise overview of education, research, experience, service, and selected honors."
author_profile: false
redirect_from:
  - /resume
---

{% assign profile = site.data.profile %}

<div class="cv-download">
  <p>Last updated August 2026.</p>
  <a class="button button--primary" href="{{ profile.cv | relative_url }}">Download PDF</a>
</div>

<section class="cv-section">
  <h2>Education</h2>
  <div class="cv-rows">
    {% for item in profile.education %}
      <article class="cv-row">
        <div><h3>{{ item.degree }}</h3><p>{{ item.institution }}</p></div>
        <div class="cv-row__meta">{% if item.status %}<p>{{ item.status }}</p>{% endif %}<p>GPA {{ item.gpa }}</p></div>
      </article>
    {% endfor %}
  </div>
</section>

<section class="cv-section">
  <h2>Research areas</h2>
  <div class="research-areas">
    {% for topic in profile.research_interests %}<span>{{ topic }}</span>{% endfor %}
  </div>
</section>

<section class="cv-section">
  <h2>Experience</h2>
  <div class="cv-rows">
    {% for item in profile.experience %}
      <article class="cv-row">
        <div><h3>{{ item.organization }}</h3><p>{{ item.role }}</p></div>
        <p class="cv-row__meta">{{ item.period }}</p>
      </article>
    {% endfor %}
  </div>
</section>

<section class="cv-section">
  <h2>Projects & open source</h2>
  <div class="cv-rows">
    {% for item in profile.other_experience %}
      <article class="cv-row">
        <div><h3>{{ item.organization }}</h3><p>{{ item.detail }}</p></div>
        {% if item.period %}<p class="cv-row__meta">{{ item.period }}</p>{% endif %}
      </article>
    {% endfor %}
  </div>
</section>

<section class="cv-section">
  <h2>Selected honors</h2>
  <ul class="honor-list">{% for item in profile.honors %}<li>{{ item }}</li>{% endfor %}</ul>
</section>

<section class="cv-section cv-section--split">
  <div>
    <h2>Reviewing</h2>
    <ul class="plain-list">{% for item in profile.reviewing %}<li>{{ item }}</li>{% endfor %}</ul>
  </div>
  <div>
    <h2>Teaching</h2>
    <ul class="plain-list">{% for item in profile.teaching %}<li>{{ item }}</li>{% endfor %}</ul>
    <h2>Community</h2>
    <ul class="plain-list">{% for item in profile.other_service %}<li>{{ item }}</li>{% endfor %}</ul>
  </div>
</section>
