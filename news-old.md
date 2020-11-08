---
layout: default
pagination:
  enabled: true
title: News
permalink: /news/
---

{% for post in paginator.posts %}
<article class="post">
    {% if post.img %}
    <a class="post-thumbnail" style="background-image: url({{"/assets/img/" | prepend: site.baseurl | append : post.img}})" href="{{post.url | prepend: site.baseurl}}"></a>
  {% else %}
  {% endif %}
  <div class="post-content">
    <h2 class="post-title"; style="font-size:100%"><a href="{% if post.link %}{{post.link}}{% else %}{{ post.url| prepend: site.baseurl}}{% endif %}">{{ post.title }}</a>{% if post.link %}<span class="link-arrow"> &rarr;</span>{% endif %}</h2>
    <span class="post-date">{{post.date | date: '%b %d, %Y'}}&nbsp;&nbsp;&nbsp;&nbsp;</span>
  </div>
</article>
{% endfor %}




<ul class="posts">
  {% for post in site.posts %}
	<li>
	  <a href="{% if post.external %}{{ post.external }}{% else %}{{ post.url }}{% endif %}">
		<span class="title">{{ post.title }}</span>
	  </a> <span class="date">{{ post.date | date: "%-d %B %Y" }}</span>
	</li>
  {% endfor %}
</ul>
