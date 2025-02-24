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
/* Section "Mes Projets" */
.projets-section {
  margin-left: 50px; /* Décale les cartes vers la droite */
}

/* Pour écrans larges */
@media (min-width: 1440px) {
  .projets-section {
    margin-left: 80px; /* Un peu plus de décalage sur très grands écrans */
  }
}

/* Pour tablettes */
@media (max-width: 1024px) {
  .projets-section {
    margin-left: 20px; /* Moins de décalage pour s’adapter aux écrans moyens */
  }
}

/* Pour mobiles */
@media (max-width: 768px) {
  .projets-section {
    margin-left: 0; /* Pas de décalage sur petits écrans */
  }
}


/* Grille des projets */
.projets-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(280px, 1fr)); /* Ajustement pour plus d’espace */
  gap: 30px; /* Augmentation de l’espace entre les cartes */
  margin-top: 20px;
  padding: 20px;
  justify-content: center;
}

/* Ajustement pour tablettes */
@media (max-width: 1024px) {
  .projets-grid {
    grid-template-columns: repeat(2, minmax(280px, 1fr)); /* 2 colonnes */
  }
}

/* Ajustement pour mobiles */
@media (max-width: 768px) {
  .projets-grid {
    grid-template-columns: repeat(1, minmax(280px, 1fr)); /* 1 colonne */
  }
}

/* Style des cartes */
.projet-card {
  background: #181818;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 6px 15px rgba(0, 0, 0, 0.5);
  transition: transform 0.2s ease-in-out, box-shadow 0.3s ease;
  max-width: 400px; /* Largeur maximale des cartes pour éviter qu’elles soient trop grandes */
  margin: auto; /* Centre les cartes si besoin */
}

.projet-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.6);
}


/* Image */
.projet-thumbnail img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-bottom: 3px solid var(--mm-custom-accent, #0ff);
}

/* Infos */
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
