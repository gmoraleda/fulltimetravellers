---
layout: default
title: "Full Time Travellers - Blog en espanol"
permalink: /es/
---

# Entradas

{% assign es_posts = site.posts | where: "lang", "es" %}
{% for post in es_posts %}
- **{{ post.date | date: "%Y-%m-%d" }}** — [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}

---

## Paginas

{% for page in site.pages %}{% if page.lang == "es" and page.url contains "/es/" and page.url != "/es/" %}
- [{{ page.title }}]({{ page.url | relative_url }})
{% endif %}{% endfor %}
