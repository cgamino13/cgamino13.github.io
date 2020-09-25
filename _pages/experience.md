---
layout: default
title: Experience
permalink: /experience/
---

{% assign iter = 0  %}
{% for exp in site.data.experience  %}
  {% if iter == 0 %}
    {% include default-left-card.html cardData = exp%}
    {% assign iter = 1  %}
  {% else %}
    {% include default-right-card.html cardData = exp%}
    {% assign iter = 0  %}
  {% endif %}
{% endfor %}
