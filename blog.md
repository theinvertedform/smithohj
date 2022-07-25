---
title: Blog
permalink: /blog
---
Rolling index of blog posts. For a list of contributors, [see here](/authors).

<article>
  {% for post in site.posts %}
      <date>{{ post.date | date: "%b %-d, %Y" }}</date>
      <a href="{{ post.url }}">{{ post.title }}</a>{% if post.author != page.author %} by {{ post.author | capitalize }}{% endif %}
      <p>{{ post.excerpt }}</p>
  {% endfor %}
</article>

