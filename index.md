---
title: Mike Stone 
header: Mike Stone 
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon 
permalink: /
layout: default
---

{% for post in site.posts %}
  <h2><a href="{{ post.url }}">{{ post.post_title }}</a></h2>
  {{ post.date | date_to_string }}

  {{ post.excerpt }}<br>
{% endfor %}
