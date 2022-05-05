---
title: Index
---

This is the personal website of John Smith. Read more about me and other contributors to this website in the [About](/about) section. Check out my [blog](/blog) for a rolling list of my insane ramblings. If you want to get in touch, head on over to the [contact](/contact) page. The [Archives](/archives) contains a comprehensive index of blog posts and other writings, arranged by date, category, and tag.

{% for category in site.categories %}
  <li><a name="{{ category | first }}">{{ category | first }}</a>
    <ul>
    {% for post in category.last %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
    </ul>
  </li>
{% endfor %}

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
