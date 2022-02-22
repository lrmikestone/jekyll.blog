---
title: Mike Stone
header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
permalink: /
layout: default
---

{% for post in site.posts limit:10 %}
  <h2 class="post-link"><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <p class="meta">{{ post.date | date: "%B %-d, %Y" }}</p>

  {:.excerpt}
  {{ post.excerpt }}
{% endfor %}

<script>
  if (window.netlifyIdentity) {
    window.netlifyIdentity.on("init", user => {
      if (!user) {
        window.netlifyIdentity.on("login", () => {
          document.location.href = "/admin/";
        });
      }
    });
  }
</script>
