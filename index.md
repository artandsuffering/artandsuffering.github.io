---
layout: default
title: Home
---
<section id="latestposts">
	<header><h2>Latest posts</h2></header>
	{% assign posts_by_year = site.posts | group_by_exp:"post", "post.date | date: '%Y'" %}
	<ul>
		{% for year in posts_by_year %}
			<li>
				<h3>{{ year.name }}</h3>
				{% assign posts_by_month = year.items | group_by_exp:"post", "post.date | date: '%B'" %}
				<ul>
					{% for month in posts_by_month %}
						<li>
							<h4>{{ month.name }}</h4>
							<ul>
							  {% for post in month.items %}
								<li>{% include postpreview.html %}</li>
							  {% endfor %}
							</ul>
						</li>
					{% endfor %}
				</ul>
			</li>
		{% endfor %}
	</ul>
		
</section>