---
title: "03_versions-prototype.md"
version: "v3.1"
role: "Roadmap des Livrables Techniques (V3 à V8)"
---

# 📅 Roadmap & Versions

Ce document définit le planning des livrables techniques, suivant la progression officielle du projet fil rouge (V3 à V8).

## 🟢 Version 3 : Interface Publique
**Objectif :** Mise en place de la structure Web (MVC) et de l'intégration UI.
*   **Livrable :** Site vitrine avec données simulées (Mock).
*   **Contenu :**
    *   Setup Laravel & Tailwind CSS.
    *   Contrôleurs Publics (`HomeController`, `ArticleController`).
    *   Vues Blade : Liste des articles, Page Détail.

## 🔵 Version 4 : Base de Données
**Objectif :** Rendre l'application dynamique.
*   **Livrable :** Site connecté à MySQL.
*   **Contenu :**
    *   Modélisation (MCD/MLD) : Tables `articles`, `categories`, `users`.
    *   Migrations & Seeders (Factory).
    *   Modèles Eloquent & Relations.
    *   Connexion des vues V3 à la Base de Données.

## 🟠 Version 5 : Back-Office Admin
**Objectif :** Gestion des contenus (CRUD).
*   **Livrable :** Espace Admin fonctionnel.
*   **Contenu :**
    *   Layout Admin (Sidebar, Dashboard).
    *   CRUD complet Article (Create, Read, Update, Delete).
    *   Gestion de l'Upload d'images.

## 🔴 Version 6 : Sécurité & Permissions
**Objectif :** Sécuriser les accès.
*   **Livrable :** Authentification et Gestion des Rôles.
*   **Contenu :**
    *   Authentification (Laravel Fortify/Breeze).
    *   Intégration **Spatie Laravel Permission**.
    *   Rôles : `Admin` (Tout accès) vs `Editeur` (Ses propres articles).
    *   Middleware & Policies.

## 🟣 Version 7 : API REST
**Objectif :** Ouvrir les données.
*   **Livrable :** Endpoints JSON documentés.
*   **Contenu :**
    *   API Resources (Transformation de données).
    *   Endpoints : `GET /api/articles`, `GET /api/articles/{id}`.
    *   Pagination & Filtres.
    *   Tests API (Postman / Pest).

## 📱 Version 8 : Application Mobile
**Objectif :** Client natif Android.
*   **Livrable :** APK Android connecté.
*   **Contenu :**
    *   Projet Kotlin Jetpack Compose.
    *   Client HTTP (Retrofit) consommant l'API V7.
    *   Écrans : Liste des articles, Détail Article.
    *   Gestion des états de chargement/erreur.
