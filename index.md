---
title: "Bienvenue"
layout: home
author_profile: true
---

## 🚀 Mes Projets  

<div class="cards">
  {% for projet in site.projets %}
  <div class="card">
    <a href="{{ projet.url }}">
      <img src="{{ projet.header.image }}" alt="{{ projet.title }}" />
      <h3>{{ projet.title }}</h3>
    </a>
    <p>{{ projet.date | date: "%d/%m/%Y" }}</p>
  </div>
  {% endfor %}
</div>

<style>
.cards {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 20px;
}

.card {
  border: 1px solid #ddd;
  padding: 10px;
  border-radius: 5px;
  text-align: center;
  background: white;
}

.card img {
  max-width: 100%;
  height: auto;
  border-radius: 5px;
}
</style>
