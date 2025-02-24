---
title: "Bienvenue"
layout: home
author_profile: true
---

## 🚀 Mes Projets  

<div class="projets-grid">
  {% for projet in site.projets %}
  <div class="projet-card">
    <a href="{{ projet.url }}">
      <div class="projet-thumbnail">
        <img src="{{ projet.header.image }}" alt="{{ projet.title }}">
      </div>
      <div class="projet-info">
        <h3>{{ projet.title }}</h3>
        <p class="projet-date">{{ projet.date | date: "%d/%m/%Y" }}</p>
      </div>
    </a>
  </div>
  {% endfor %}
</div>

<style>
/* Grille des projets */
.projets-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 20px;
  margin-top: 20px;
}

/* Carte de projet */
.projet-card {
  background: var(--mm-custom-background, #111);
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
  transition: transform 0.2s ease-in-out, box-shadow 0.3s ease;
}

.projet-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 6px 15px rgba(0, 0, 0, 0.4);
}

/* Image de prévisualisation */
.projet-thumbnail img {
  width: 100%;
  height: 180px;
  object-fit: cover;
  border-bottom: 2px solid var(--mm-custom-accent, #0ff);
}

/* Infos du projet */
.projet-info {
  padding: 15px;
  text-align: center;
}

.projet-info h3 {
  font-size: 1.4em;
  color: var(--mm-custom-text, #fff);
  margin-bottom: 5px;
}

.projet-date {
  font-size: 0.9em;
  color: var(--mm-custom-muted, #bbb);
}
</style>
