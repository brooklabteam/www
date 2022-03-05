---
layout: default
pagination:
  enabled: true
title: News
permalink: /news
---
{% for post in site.posts %}
<article class="post">
  <div class="post-image" style="float:left; width:200px;">
    {% if post.img %}
    <a class="post-thumbnail" href="{% if post.link %}{{post.link}}{% else %}{{ post.url| prepend: site.baseurl}}{% endif %}">{{ post.title }}">
      <img src="{{"/assets/img/" | prepend: site.baseurl | append : post.img}}"/>
    </a>
  </div>
  {% else %}
  {% endif %}
  <div class="post-content" style="float:left; margin-left:2em; max-width:500px;">

    <a href="{% if post.link %}{{post.link}}{% else %}{{ post.url| prepend: site.baseurl}}{% endif %}">{{ post.title }}</a>

    {% if post.link %}
      <span class="link-arrow"> &rarr;</span>
    {% endif %}

    <br/>

    <span class="post-date">{{post.date | date: '%b %d, %Y'}}&nbsp;&nbsp;&nbsp;&nbsp;</span>
  </div>
</article>

<div style="clear:both;">&nbsp;</div>
 
{% endfor %}


  
