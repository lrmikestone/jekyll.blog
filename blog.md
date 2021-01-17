---
layout: default
title: Mike's Blog
header: Mike's Blog
description: Thoughts Too Verbose For Social Media
permalink: /blog/
---

{% for post in site.posts %}
  {{ post.date | date_to_string }} - <a href="{{ post.url }}">{{ post.title }}</a><br>
{% endfor %}
