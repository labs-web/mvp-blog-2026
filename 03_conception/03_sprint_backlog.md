---
title: "03_sprint_backlog.md"
version: "v4.0"
role: "Sprint Backlog & Roadmap (V3 à V8)"
---

# 📅 Sprint Backlog & Roadmap

Ce document définit les fonctionnalités à implémenter par Sprint (anciennement Versions), servant de Backlog produit.

## 🟢 Sprint 3 : Interface Publique (Intégration)
**Objectif :** Mise en place de la structure Web (MVC) et de l'intégration UI.
*   **User Stories :**
    *   En tant que visiteur, je veux voir la page d'accueil pour découvrir les derniers articles.
    *   En tant que visiteur, je veux lire un article complet.
*   **Tâches Techniques :**
    *   Setup Laravel 12 & Laravel UI (Tailwind CSS).
    *   Contrôleurs Publics (`HomeController`, `ArticleController`).
    *   Vues Blade : Liste des articles, Page Détail.

## 🔵 Sprint 4 : Base de Données
**Objectif :** Rendre l'application dynamique.
*   **User Stories :**
    *   En tant que développeur, je veux une base de données structurée pour stocker les articles.
*   **Tâches Techniques :**
    *   Modélisation (MCD/MLD) : Tables `articles`, `categories`, `users`.
    *   Migrations & Seeders (Factory).
    *   Modèles Eloquent & Relations.
    *   Connexion des vues Sprint 3 à la Base de Données.

## 🟠 Sprint 5 : Back-Office Admin
**Objectif :** Gestion des contenus (CRUD).
*   **User Stories :**
    *   En tant qu'admin, je veux créer et gérer des articles.
*   **Tâches Techniques :**
    *   Layout Admin (Sidebar, Dashboard).
    *   CRUD complet Article (Create, Read, Update, Delete).
    *   Gestion de l'Upload d'images.

## 🔴 Sprint 6 : Sécurité & Permissions
**Objectif :** Sécuriser les accès.
*   **User Stories :**
    *   En tant qu'éditeur, je veux me connecter pour gérer mes articles.
    *   En tant qu'admin, je veux gérer les rôles.
*   **Tâches Techniques :**
    *   Authentification (Laravel UI).
    *   Intégration **Spatie Laravel Permission**.
    *   Rôles : `Admin` vs `Editeur`.
    *   Middleware & Policies.

## 🟣 Sprint 7 : API REST
**Objectif :** Ouvrir les données.
*   **User Stories :**
    *   En tant que développeur mobile, je veux une API pour récupérer les articles.
*   **Tâches Techniques :**
    *   API Resources (Transformation de données).
    *   Endpoints : `GET /api/articles`, `GET /api/articles/{id}`.
    *   Pagination & Filtres.
    *   Tests API (Postman / Pest).

## 📱 Sprint 8 : Application Mobile
**Objectif :** Client natif Android.
*   **User Stories :**
    *   En tant qu'utilisateur mobile, je veux lire les articles sur mon téléphone.
*   **Tâches Techniques :**
    *   Projet Kotlin Jetpack Compose.
    *   Client HTTP (Retrofit) consommant l'API Sprint 7.
    *   Écrans : Liste des articles, Détail Article.
    *   Gestion des états de chargement/erreur.
