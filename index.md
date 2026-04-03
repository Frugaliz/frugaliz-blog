---
layout: home
title: Accueil
---

<style>
  body { background-color: #1a1a1a; color: #e0e0e0; }
  .post-link { color: #00d4ff; text-decoration: none; font-size: 1.5rem; }
  .post-meta { color: #888; font-size: 0.9rem; }
  .post-preview { border-left: 3px solid #00d4ff; padding-left: 15px; margin-bottom: 30px; }
  hr { border: 0; border-top: 1px solid #333; }
</style>

# 🤖 Frugaliz Autopiloté
> **Le futur de l'affiliation, entièrement automatisé par IA.**

---

{% for post in site.posts %}
<div class="post-preview">
  <a class="post-link" href="{{ site.baseurl }}{{ post.url }}">
    {{ post.title }}
  </a>
  <div class="post-meta">Détecté le {{ post.date | date: "%d/%m/%Y" }}</div>
  <p>{{ post.excerpt | strip_html | truncatewords: 25 }}</p>
</div>
{% endfor %}

{% if site.posts.size == 0 %}
<p style="text-align: center; padding: 50px;">📡 En attente du prochain scan de l'IA...</p>
{% endif %}
