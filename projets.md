---
title: "Projets"
layout: single
permalink: /projets/
---

{% for projet in site.projets %}
- [{{ projet.title }}]({{ projet.url }}) - {{ projet.date | date: "%d/%m/%Y" }}
{% endfor %}
