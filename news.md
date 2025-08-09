---
layout: page
pagination:
  enabled: true
title: News
permalink: /news
---
{% for post in site.posts %}
<article class="post">
  <div class="post-image" class="float-start col-md-3">
    <a class="post-thumbnail" href="{% if post.link %}{{post.link}}{% else %}{{ post.url| prepend: site.baseurl}}{% endif %}">
      <img src="{{"/assets/img/" | prepend: site.baseurl | append : post.img}}" class="img-fluid" />
    </a>
  </div>
  <div class="post-content" style="float:left; margin-left:2em; max-width:500px;" markdown="1">

    <a href="{% if post.link %}{{post.link}}{% else %}{{ post.url| prepend: site.baseurl}}{% endif %}">{{ post.title }}{% if post.link %}<span class="link-arrow"> ↗</span>{% endif %}</a>\

    <span class="post-date">{{post.date | date: '%b %d, %Y'}}&nbsp;&nbsp;&nbsp;&nbsp;</span>
  </div>
</article>

<div style="clear:both;">&nbsp;</div>
 
{% endfor %}
