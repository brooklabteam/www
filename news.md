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
   <a href="{% if post.external %}{{ post.external }}{% else %}{{ post.url }}{% endif %}">
		<span class="title">{{ post.title }}</span>
	  </a> <span class="date">{{ post.date | date: "%-d %B %Y" }}</span>
  </div>
  {% endfor %}
</article>
