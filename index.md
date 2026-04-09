---
layout: default
title: Full Time Travellers
---

<p class="home-intro">Travel blog archive &mdash; 2016/2017</p>

<h2>Espanol</h2>
{% assign es_posts = site.posts | where: "lang", "es" %}
{% for post in es_posts limit: 5 %}
<div class="post-entry">
  <span class="date">{{ post.date | date: "%d.%m.%Y" }}</span>
  <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
</div>
{% endfor %}
<p><a href="{{ '/es/' | relative_url }}">Todas las entradas &rarr;</a></p>

<hr>

<h2>Deutsch</h2>
{% assign de_posts = site.posts | where: "lang", "de" %}
{% for post in de_posts limit: 5 %}
<div class="post-entry">
  <span class="date">{{ post.date | date: "%d.%m.%Y" }}</span>
  <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
</div>
{% endfor %}
<p><a href="{{ '/de/' | relative_url }}">Alle Beitrage &rarr;</a></p>
