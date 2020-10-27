---
layout: default
pagination:
  enabled: true
title: News
permalink: /news/
---
<article class="post">
  {% for post in site.posts %}
	 {% if post.img %}
    <a class="post-thumbnail" style="background-image: url({{"/assets/img/" | prepend: site.baseurl | append : post.img}})" href="{% if post.external %}{{ post.external }}{% else %}{{ post.url }}{% endif %}"></a>
  {% else %}
  {% endif %}
  <div class="post-content">
   <a href="{% if post.external %}{{ post.external }}{% else %}{{ post.url }}{% endif %}">
		<span class="title">{{ post.title }}</span>
	  </a> <span class="date">{{ post.date | date: "%-d %B %Y" }}</span>
  </div>
  {% endfor %}
</article>
