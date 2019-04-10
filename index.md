---
layout: default
title: Home
---
<section>
	<header>Latest posts</header>

	<ul>
		{% for post in site.posts %}
			<li>
				<a href="{{ post.url }}">{{ post.title }} ({{ post.date | date_to_string}})</a>
				{{ post.excerpt | truncatewords:65 }}
			</li>
		{% endfor %}
	</ul>
</section>