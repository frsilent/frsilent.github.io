---
title: Portfolio
layout: default
---

{% for post in site.posts %}
<div class="post">
    {{ post.content }}
    <div class="well well-sm">
        <a href="{{ post.url }}">Permalink</a>
<!--         <div class="btn-group sharing">
            <button class="btn btn-default btn-xs disabled">Share:</button>
            <a class="btn btn-default btn-xs" target="_blank" title="Like on Facebook" href="http://www.facebook.com/plugins/like.
                    php?href={{ post.url }}">
                <i class="fb fb-thumbs-o-up fb-lg fb"></i>
            </a>
        </div> -->
        <div class="btn-group">
          <button class="btn btn-default btn-xs disabled">Share:</button>
            <a class="btn btn-default btn-xs" target="_blank" title="Like On Facebook" href="http://www.facebook.com/plugins/like.php?href={{ post.url }}">
                <i class="fa fa-thumbs-o-up fa-lg fb"></i>
            </a>
            <a class="btn btn-default btn-xs google-plus-one" target="_blank" title="+1 On Google" href="https://apis.google.com/_/+1/fastbutton?usegapi=1&amp;size=large&amp;hl=en&amp;url={{ post.url }}">
                <i class="fa fa-google-plus fa-2x google"></i>
                <span class="google">1</span>
            </a>
            <a class="btn btn-default btn-xs" target="_blank" title="On Facebook" href="http://www.facebook.com/sharer.php?u={{ post.url }}&amp;t=Social%20Buttons%20in%20HTML%20only%20using%20Twitter%20Bootstrap%203%20and%20Font%20Awesome%20Icons">
                <i class="fa fa-facebook fa-lg fb"></i>
            </a>
            <a class="btn btn-default btn-xs" target="_blank" title="On Twitter" href="http://twitter.com/share?url={{ post.url }}&amp;text=Social%20Buttons%20in%20HTML%20only%20using%20Twitter%20Bootstrap%203%20and%20Font%20Awesome%20Icons">
                <i class="fa fa-twitter fa-lg tw"></i>
            </a>
            <a class="btn btn-default btn-xs" target="_blank" title="On Google Plus" href="https://plusone.google.com/_/+1/confirm?hl=en&amp;url={{ post.url }}">
                <i class="fa fa-google-plus fa-lg google"></i>
            </a>
            <a class="btn btn-default btn-xs" target="_blank" title="On LinkedIn" href="http://www.linkedin.com/shareArticle?mini=true&amp;url={{ post.url }}">
                <i class="fa fa-linkedin fa-lg linkin"></i>
            </a>
        </div>
        <span class="post-category-list">[{% for category in post.categories %}
            <a href="/categories/{{ category }}/">{{ category }}</a>
            {% unless forloop.last %},{% endunless %}
            {% endfor %}]
        </span>
    </div>
</div>
{% endfor %}
