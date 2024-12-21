---
layout: tag
title: "Tag: faith"
tag: faith
permalink: /tags/faith
---

<h1>Posts tagged with "{{ page.tag }}"</h1>
<ul>
  {% for post in site.posts %}
    {% if post.tags contains page.tag %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>