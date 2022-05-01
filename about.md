---
layout: default
title: About
permalink: /about
---

# About the Northstar

A new media going against the grain of the corporate press and the elites.

# Masthead

<ul>
  {% for author in site.authors %}
    <li>
      <h2><a href="{{ author.url }}">{{ author.name }}</a></h2>
      <h3>{{ author.position }}</h3>
      <p>{{ author.content | markdownify }}</p>
    </li>
  {% endfor %}
</ul>
