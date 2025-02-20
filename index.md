---
layout: home
title: "Bienvenue sur mon Portfolio"
author_profile: true
entries_layout: grid
---

## 🎮 Mes Projets

{% for project in site.projets %}
  {% include archive-single.html type="grid" %}
{% endfor %}
