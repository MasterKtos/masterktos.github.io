---
layout: default
title: Games
---

{% for item in site.data.games %}

# {{item.name}}
> {{ item.description }}

<dl>
{% for detail in item.details %}
<dt>{{ detail.name }}</dt>
<dd>{{ detail.description }}</dd>
{% endfor %}
</dl>

<section>
{% if item contains "itchio_link" %}
<a href="{{ item.itchio_link }}" class="btn">itch.io</a>
{% endif %}
{% if item contains "repo_link" %}
<a href="{{ item.repo_link }}" class="btn btn-github"><span class="icon"></span>View on GitHub</a>
{% endif %}
</section>

{% endfor %}
