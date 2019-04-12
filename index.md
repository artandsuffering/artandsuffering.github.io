---
layout: default
title: Home
---
<section>
	<header><h2>Latest posts</h2></header>
	<ul>
		{% for post in site.posts %}
			<li>
				{% include postpreview.html %}
			</li>
		{% endfor %}
	</ul>
</section>