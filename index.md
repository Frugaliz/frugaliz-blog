---
layout: home
title: Accueil
---

# 🚀 Derniers Bons Plans Frugaliz

Voici les pépites dénichées par l'IA aujourd'hui :

{% for post in site.posts %}
### [{{ post.title }}]({{ post.url }})
*Publié le {{ post.date | date: "%d/%m/%Y" }}*
{{ post.excerpt | strip_html | truncatewords: 30 }}

---
{% endfor %}
