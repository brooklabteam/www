---
layout: default
pagination:
  enabled: true
title: News
permalink: /news/
---
{% for post in site.posts %}
<article class="post">
<a class="post-thumbnail" style="background-image: url({{"/assets/news/" | prepend: site.baseurl | append : post.img}})" href="{{post.url | prepend: site.baseurl}}"></a>
</article>
{% endfor %}