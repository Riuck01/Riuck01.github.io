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
.projets-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); /* Responsive grid */
  gap: 20px; /* Space between cards */
  width: 85%; /* Adjust width to fit better */
  margin: 0 auto; /* Center the grid */
  padding: 20px 0;
}

/* Ensuring the description has enough space */
.container { 
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  gap: 40px; /* Space between description and projects */
}

/* Description panel */
.description {
  flex: 1; /* Takes up remaining space */
  max-width: 400px; /* Prevents it from being too wide */
}

/* Adjustments for larger screens */
@media (min-width: 1440px) {
  .projets-grid {
    width: 90%;
  }
}

/* Adjustments for tablets */
@media (max-width: 1024px) {
  .container {
    flex-direction: column;
    align-items: center;
  }
  .description {
    max-width: 100%; /* Full width for small screens */
    text-align: center;
  }
}

/* Mobile adjustments */
@media (max-width: 768px) {
  .projets-grid {
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); /* Smaller cards on mobile */
    width: 100%;
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
