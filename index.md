---
title: "Bienvenue"
layout: home
author_profile: true
---

## 🚀 Mes Projets  

<div class="projets-grid">
  {% for projet in site.projets reversed %}
  <div class="projet-card">
    <a href="{{ projet.url }}">
      <div class="projet-thumbnail">
        <img src="{{ projet.header.image }}" alt="{{ projet.title }}">
        <div class="overlay"></div>
      </div>
      <div class="projet-info">
        <h3>{{ projet.title }}</h3>
      </div>
    </a>
  </div>
  {% endfor %}
</div>

<style>
/* ✅ Grid Layout */
.projets-grid {
  display: grid;
  grid-template-columns: repeat(1, 1fr); /* Par défaut : 1 colonne */
  gap: 25px;
  width: 90%;
  margin: 0 auto;
  padding: 20px 0;
}

/* 🖥️ PC - 2 colonnes */
@media (min-width: 1024px) {
  .projets-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

/* 📱 Mobile - 1 colonne */
@media (max-width: 768px) {
  .projets-grid {
    grid-template-columns: repeat(1, 1fr);
    width: 100%;
  }
}

/* 🎨 ✅ Card Style */
.projet-card {
  background: #181818;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 6px 15px rgba(0, 0, 0, 0.5);
  transition: transform 0.3s ease-in-out, box-shadow 0.3s ease;
  max-width: 400px;
  margin: auto;
  position: relative;
}

.projet-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.6);
}

/* 🎨 ✅ Thumbnail */
.projet-thumbnail {
  position: relative;
  overflow: hidden;
  height: 220px;
}

.projet-thumbnail img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.4s ease-in-out;
}

/* ✅ Hover Effect */
.projet-card:hover .projet-thumbnail img {
  transform: scale(1.1) translateY(-10px);
}

/* ✅ Overlay */
.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  opacity: 0;
  transition: opacity 0.3s ease-in-out;
}

.projet-card:hover .overlay {
  opacity: 1;
}

/* 🎨 ✅ Info */
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
