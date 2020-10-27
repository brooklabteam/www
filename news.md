---
layout: default
pagination:
  enabled: true
title: News
permalink: /news/
---
<article class="post">
  {% for post in site.posts %}
  <div class="post-content">
    <h2 class="post-title"; style="font-size:100%"><a href="{% if post.link %}{{post.link}}{% else %}{{ post.url| prepend: site.baseurl}}{% endif %}">{{ post.title }}</a>{% if post.link %}<span class="link-arrow"> &rarr;</span>{% endif %}</h2>
    <span class="post-date">{{post.date | date: '%b %d, %Y'}}&nbsp;&nbsp;&nbsp;—&nbsp;</span>
  </div>
  {% endfor %}
</article>
