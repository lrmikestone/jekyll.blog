---
title: Mike Stone 
header: Mike Stone 
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon 
permalink: /
layout: default
---

# Welcome!!

You've reached my blog. I might be here, and I might not. It's hard to tell because I'm writing this in the past, and you're there in the future. Or the present? Time, it's so weird.

Anyway, content....

{% for post in site.posts %}
  <p><h2><a href="{{ post.url }}">{{ post.title }}</a></h2><br>
  {{ post.date | date_to_string }}</p>

{{ post.description }}<br>
{% endfor %}
