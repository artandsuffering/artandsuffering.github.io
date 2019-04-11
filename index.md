---
layout: default
title: Home
---
<section>
	<header>Latest posts</header>
	<ul>
		{% for post in site.posts %}
			<li>
				{% include postpreview.html %}
			</li>
		{% endfor %}
	</ul>
</section>