---
title: Portfolio
layout: default
---

{% for post in site.posts %}
{{ post.content }}
[permalink]({{ post.url }})
{% endfor %}
