---
title: Portfolio
layout: default
---

{% for post in site.posts %}
<div class="post">
    {{ post.content }}
    <div class="well well-sm">
        <a href="{{ post.url }}">Permalink</a>
        <div class="post-category-list">[{% for category in post.categories %}
            <a href="/categories/{{ category }}/">{{ category }}</a>
            {% unless forloop.last %},{% endunless %}
            {% endfor %}]
        </div>
    </div>
</div>
{% endfor %}
