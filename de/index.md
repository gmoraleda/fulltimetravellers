---
layout: default
title: Deutsch
permalink: /de/
lang: de
---

<nav class="sub-nav">
{% for pg in site.pages %}{% if pg.lang == "de" and pg.url contains "/de/" and pg.url != "/de/" %}<a href="{{ pg.url | relative_url }}">{{ pg.title }}</a> {% endif %}{% endfor %}
</nav>

{% assign de_posts = site.posts | where: "lang", "de" %}
{% for post in de_posts %}
<div class="post-entry">
  <span class="date">{{ post.date | date: "%d.%m.%Y" }}</span>
  <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
</div>
{% endfor %}
