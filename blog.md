---
layout: default
title: Mike's Blog
header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
permalink: /blog/
---

{% assign postsByYear = site.posts | group_by_exp:"post", "post.date | date: '%Y'" %}
{% for year in postsByYear %}
<h1>{{ year.name }}</h1>
{% assign postsByMonth = year.items | group_by_exp:"post", "post.date | date: '%B'" %}
{% for month in postsByMonth %}
<h2>{{ month.name }}</h2>
<ul class="archive">
{% for post in month.items %}
<li><b><a href="{{ post.url }}">{{ post.title }}</a></b></li>
{% endfor %}
</ul>
{% endfor %}
{% endfor %}
