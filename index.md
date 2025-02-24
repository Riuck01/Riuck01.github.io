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
/* Grille des projets (3 par ligne) */
.projets-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 20px;
  margin-top: 20px;
  padding: 0 10px;
}

/* Carte de projet */
.projet-card {
  background: #181818;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 6px 15px rgba(0, 0, 0, 0.5);
  transition: transform 0.2s ease-in-out, box-shadow 0.3s ease;
}

.projet-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.6);
}

/* Image de prévisualisation */
.projet-thumbnail img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-bottom: 3px solid var(--mm-custom-accent, #0ff);
}

/* Infos du projet */
.projet-info {
  padding: 15px;
  text-align: center;
}

.projet-info h3 {
  font-size: 1.5em;
  color: #fff;
  margin-bottom: 5px;
}

.projet-date {
  font-size: 1em;
  color: #bbb;
}
</style>
