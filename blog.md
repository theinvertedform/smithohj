---
title: Blog
permalink: /blog
---
Rolling index of blog posts. For a list of contributors, [see here](/authors)!

{% for post in site.posts %}
<article>
	<date>{{ post.date | date: "%b %-d, %Y" }}</date>
	<a href="{{ post.url }}">{{ post.title }}</a>
	{% assign author = site.data.authors[post.author] %}
	{% if author %}
	by {{ author.name }}
	{% else %}
	by {{ site.author.name }}
	{% endif %}
    <p>{{ post.excerpt }}</p>
</article>
{% endfor %}
