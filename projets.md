---
title: "Projets"
layout: single
permalink: /projets/
---

## Mes Projets 🎮  

{% for projet in site.projets %}
- **[{{ projet.title }}]({{ projet.url }})** - *{{ projet.date | date: "%d/%m/%Y" }}*
{% endfor %}
