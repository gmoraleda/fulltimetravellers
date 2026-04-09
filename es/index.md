---
layout: default
title: Español
permalink: /es/
lang: es
---

<nav class="sub-nav">
{% for pg in site.pages %}{% if pg.lang == "es" and pg.url contains "/es/" and pg.url != "/es/" %}<a href="{{ pg.url | relative_url }}">{{ pg.title }}</a> {% endif %}{% endfor %}
</nav>

{% assign es_posts = site.posts | where: "lang", "es" %}
{% for post in es_posts %}
<div class="post-entry">
  <span class="date">{{ post.date | date: "%d.%m.%Y" }}</span>
  <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
</div>
{% endfor %}
