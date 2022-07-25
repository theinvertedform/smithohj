---
layout: default
title: Contributors
---

On my personal website, I occasionally publish writing by people other than myself. This may be for test purposes, or it may be for purposes of spreading something that I think is important. Below is an index of such authors, with links to their contributions.

{% for author in site.authors %}
<section>
<h2 id="{{ author.name | slugify }}"><a href="{{ author.url }}">{{ author.name }}</a></h2>
<p>{{ author.content | markdownify }}</p>
<ul>
{% assign filtered_posts = site.posts | where: 'author', author.short_name %}
{% for post in filtered_posts %}
  <li><a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
</section>
{% endfor %}
