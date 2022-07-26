---
title: index
# layout: home
---

This is the personal website of John Smith. Read more about me and other contributors to this website in the [About](/about) section. Check out my [blog](/blog) for a rolling list of my insane ramblings. If you want to get in touch, head on over to the [contact](/contact) page. The [Archives](/archives) contains a comprehensive index of blog posts and other writings, arranged by date, category, and tag.

<section id="blog" class="index-category">
<h3>Blog Posts</h3>
<ul>
{% for post in site.categories.blog %}
<li><a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
</section>

{% for category in site.categories %}
{% unless category contains "blog" %}
<section id="{{ category[0] }}" class="index-category">
<h3>{{ category[0] | capitalize }}</h3>
<ul>
    {% for post in category[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
</section>
{% endunless %}
{% endfor %}
