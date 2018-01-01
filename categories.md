---
layout: page
title: Catégories
permalink: /categories/
---

{% for category in site.categories %}

## {{ category | first }}

{% for posts in category %}
{% for post in posts %}
{% if post.url %}

* [{{ post.title }}]({{ post.url }}) ({{ post.date | date: "%Y-%m-%d"}})

{% endif %}
{% endfor %}
{% endfor %}
{% endfor %}
