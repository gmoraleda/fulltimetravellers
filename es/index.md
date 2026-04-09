---
layout: default
title: Espanol
permalink: /es/
lang: es
---

{% for page in site.pages %}{% if page.lang == "es" and page.url contains "/es/" and page.url != "/es/" %}[{{ page.title }}]({{ page.url | relative_url }}) | {% endif %}{% endfor %}

---

{% assign es_posts = site.posts | where: "lang", "es" %}
{% for post in es_posts %}
**{{ post.date | date: "%d.%m.%Y" }}** — [{{ post.title }}]({{ post.url | relative_url }})

{% endfor %}
