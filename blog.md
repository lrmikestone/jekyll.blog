---
layout: default
title: Mike's Blog
header: Mike's Blog
description: Thoughts Too Verbose For Social Media
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
<li><b><a href="{{ post.url }}">{{ post.title }}</a></b><br>{{ post.date | date_to_string }}</li>
{% endfor %}
</ul>
{% endfor %}
{% endfor %}
