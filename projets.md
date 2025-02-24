---
title: "Bienvenue"
layout: home
author_profile: true
---

## 🚀 Mes Projets  

{% for projet in site.projets %}
- **[{{ projet.title }}]({{ projet.url }})**  
  *{{ projet.date | date: "%d/%m/%Y" }}*  
  ![Preview]({{ projet.header.image }})
{% endfor %}
