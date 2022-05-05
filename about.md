---
layout: default
title: About
permalink: /about
---

# About Me

![The author on a night out spent in.](/assets/images/20220122-0330-001_cropped.JPG)

John Smith is a quirky little weirdo who is allegedly from Northern Quebec, despite being a dirty Anglophone.

# Guest Authors

Here is a list of other peoples' writing that has been posted on this blog, in order to make it appear more significant of a website than it might otherwise appear to be.

<ul>
  {% for author in site.authors %}
    <li>
      <h3><a href="{{ author.url }}">{{ author.name }}</a></h3>
      <p>{{ author.content | markdownify }}</p>
    </li>
  {% endfor %}
</ul>
