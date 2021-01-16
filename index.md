---
title: Mike Stone
header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
permalink: /
layout: default
---

{% for post in site.posts %}
  <h2 class="post-link"><a href="{{ post.url }}">{{ post.post_title }}</a></h2>
  <p class="meta">{{ post.date | date_to_string }}</p>

  {:.excerpt}
  {{ post.excerpt }}
{% endfor %}
