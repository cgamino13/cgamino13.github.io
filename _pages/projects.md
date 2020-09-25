---
layout: default
title: Projects
permalink: /projects/
---

{% assign iter = 0  %}
{% for exp in site.data.projects  %}
  {% if iter == 0 %}
    {% include default-left-card.html cardData = exp%}
    {% assign iter = 1  %}
  {% else %}
    {% include default-right-card.html cardData = exp%}
    {% assign iter = 0  %}
  {% endif %}
{% endfor %}
