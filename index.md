---
layout: default
title: Home
---
<section id="latestposts">
	<header><h2>Stickied</h2></header>
	<ul>
		{% for post in site.posts %}
			{% if post.stickied == true %}
				<li>{% include postpreview.html %}</li>
			{% endif %}
		{% endfor %}
	</ul>
		
</section>

<section id="latestposts">
	<header><h2>Latest posts</h2></header>
	{% assign posts_by_year = site.posts | group_by_exp:"post", "post.date | date: '%Y'" %}
	<ul>
		{% for year in posts_by_year %}
			<li>
				{% assign posts_by_month = year.items | group_by_exp:"post", "post.date | date: '%B'" %}
				<ul>
					{% for month in posts_by_month %}
						<li>
							<h3 class="sans">{{ month.name }} {{ year.name }}</h3>
							<ul>
							  {% for post in month.items %}
								<li>{% include postpreview.html %}</li>
							  {% endfor %}
							</ul>
							<br class="sans">
						</li>
					{% endfor %}
				</ul>
				<br class="sans">
			</li>
		{% endfor %}
	</ul>
		
</section>