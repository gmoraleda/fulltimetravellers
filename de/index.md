---
layout: default
title: "Full Time Travellers - Blog auf Deutsch"
permalink: /de/
---

# Beitrage

{% assign de_posts = site.posts | where: "lang", "de" %}
{% for post in de_posts %}
- **{{ post.date | date: "%Y-%m-%d" }}** — [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}

---

## Seiten

{% for page in site.pages %}{% if page.lang == "de" and page.url contains "/de/" and page.url != "/de/" %}
- [{{ page.title }}]({{ page.url | relative_url }})
{% endif %}{% endfor %}
