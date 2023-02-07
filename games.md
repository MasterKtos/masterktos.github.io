---
layout: default
title: Games
---

{% for item in site.data.games %}
# {{item.name}}
{% include {{item.link}} %}
{% endfor %}
