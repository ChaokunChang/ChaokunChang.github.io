---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

Biathlon: Harnessing Model Resilience for Accelerating ML Inference Pipelines. [paper](https://arxiv.org/abs/2405.11191), [code](https://github.com/ChaokunChang/Biathlon)

Is Network the Bottleneck of Distributed Training? [paper](https://arxiv.org/pdf/2006.10103), [code](https://github.com/netx-repo/training-bottleneck)

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
