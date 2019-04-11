---
layout: default
title: Home
---
<section>
	<header>Latest posts</header>
	<p>{{ site.theme }}</p>
	<ul>
		{% for post in site.posts %}
			<li>
				{% include postpreview.html %}
			</li>
		{% endfor %}
	</ul>
</section>