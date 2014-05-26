---
title: Portfolio
layout: default
---

{% for post in site.posts %}
{{ post.content }}
    <a href="{{ post.url }}">Permalink</a>
{% endfor %}
