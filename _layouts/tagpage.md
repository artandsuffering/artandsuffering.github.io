---
layout: default
---

<p>{{ page.title }}</p>

<ul>
{% for post in site.tags[page.tag] %}
  <li><a href="{{ post.url }}">{{ post.title }}</a>
      <p>{{ post.excerpt }}</p>
  </li>
{% endfor %}
</ul>
</div>
<hr>