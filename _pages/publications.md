---
layout: academic-page
permalink: /publications/
title: "Publications"
eyebrow: "Research output"
intro: "Research on agentic systems, LLM serving, video analytics, ML inference pipelines, and distributed training."
author_profile: false
---

<div class="publication-list publication-list--all">
  {% for publication in site.data.publications %}
    <article class="publication-item">
      <p class="publication-item__number">{{ forloop.index | prepend: '0' }}</p>
      <div class="publication-item__body">
        <div class="publication-item__title-row">
          <h2>{{ publication.title }}</h2>
          <span class="publication-status">{{ publication.status }}</span>
        </div>
        <p class="publication-item__authors">{{ publication.authors | replace: 'Chang, C.', '<strong>Chang, C.</strong>' }}</p>
        <p class="publication-item__venue"><span>{{ publication.venue }}</span> · {{ publication.year }}</p>
        {% if publication.links %}
          <div class="publication-item__links">
            {% for link in publication.links %}<a href="{{ link.url }}">{{ link.label }}</a>{% endfor %}
          </div>
        {% endif %}
      </div>
    </article>
  {% endfor %}
</div>
