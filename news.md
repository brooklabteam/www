---
layout: default
pagination:
  enabled: true
title: News
permalink: /news/
---
{% for post in site.posts %}
<article class="post">
    {% if post.img %}
    <a class="post-thumbnail" href="{{post.url | prepend: site.baseurl}}">
      <img src="{{"/assets/img/" | prepend: site.baseurl | append : post.img}}" style="max-width:200px;max-height:150px;"/>
    </a>
  {% else %}
  {% endif %}
  <div class="post-content">

    <a href="{% if post.link %}{{post.link}}{% else %}{{ post.url| prepend: site.baseurl}}{% endif %}">{{ post.title }}</a>

    {% if post.link %}
      <span class="link-arrow"> &rarr;</span>
    {% endif %}

    <span class="post-date">{{post.date | date: '%b %d, %Y'}}&nbsp;&nbsp;&nbsp;&nbsp;</span>
  </div>
</article>
{% endfor %}

  