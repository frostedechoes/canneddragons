---
layout: tag
title: "Tag: tech"
tag: tech
permalink: /tags/tech
---

<h1>Posts tagged with "{{ page.tag }}"</h1>
<ul>
  {% for post in site.posts %}
    {% if post.tags contains page.tag %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>