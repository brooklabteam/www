---
layout: default
pagination:
  enabled: true
title: News
permalink: /news/
---
{% for post in site.posts %}
<article class="post">
<a class="post-thumbnail" style="background-image: url({{"/assets/img/" | prepend: site.baseurl | append : post.img}})" href="{{post.url | prepend: site.baseurl}}"></a>
  <div class="post-content">
    <h2 class="post-title"; style="font-size:100%"><a href="{% if post.link %}{{post.link}}{% else %}{{ post.url| prepend: site.baseurl}}{% endif %}">{{ post.title }}</a>{% if post.link %}<span class="link-arrow"> &rarr;</span>{% endif %}</h2>
    <span class="post-date">{{post.date | date: '%b %d, %Y'}}&nbsp;&nbsp;&nbsp;—&nbsp;</span>
  </div>
</article>
{% endfor %}