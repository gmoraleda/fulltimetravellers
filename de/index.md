---
layout: default
title: Deutsch
permalink: /de/
lang: de
---

{% for page in site.pages %}{% if page.lang == "de" and page.url contains "/de/" and page.url != "/de/" %}[{{ page.title }}]({{ page.url | relative_url }}) | {% endif %}{% endfor %}

---

{% assign de_posts = site.posts | where: "lang", "de" %}
{% for post in de_posts %}
**{{ post.date | date: "%d.%m.%Y" }}** — [{{ post.title }}]({{ post.url | relative_url }})

{% endfor %}
