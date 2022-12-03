---
layout: default
title: 首页
---
<h1>漫画馆</h1>
<ul class="post-list">
	{% for post in site.posts reversed %}
	<li>
		<a href="{{ site.baseurl }}{{ post.url }}">[{{post.series}}]{{ post.title }}</a> <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
	</li>
	{% endfor %}
</ul>