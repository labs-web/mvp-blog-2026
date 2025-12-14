---
title: "04_planning_pedagogique.md"
role: "Planning des Sessions de Formation (Phases et Sprints)"
---

# 🎓 Planning Pédagogique : Fil Rouge & Mini-Projets

Ce document structure la formation en **Phases**. Une phase peut contenir **une ou plusieurs sessions** et suit une progression rigoureuse : **Imiter (N1)** > **Adapter (N2)** > **Live coding** > **Transposer (N3 Individuel)** > **Consolider (Rattrapage Groupe)**.

---

## 🗓️ Phase 1 : Fondamentaux (S1-S2)

### Session S1 : Rappels PHP & Algorithmique
*   **Objectif :** Sécuriser les bases.
*   **Contenu :** Variables, boucles, fonctions, manipulation de tableaux.

### Session S2 : Initiation Mobile (Android/Kotlin)
*   **Objectif :** Découverte de l'environnement Android Studio.
*   **Contenu :** les base de kotlin, "Hello World", Layouts simples., 

<!-- TOIDO : la fin de pahse : Présentation de planning anuelle : Projet file rouge,

Projet individuel : Blog sur une ville 
Projet en groupe : Blog de Solicode

Les session de formation,  session de rattrapage et réalisation de sprint de projet en groupe
 
 -->


---

## 🗓️ Phase 2 : Découverte Framework

### Session S3 : Lancement Laravel
**Thème :** Architecture MVC, Routing, Controller, Blade.

*   **N1 (Imiter) : Page Accueil Basique**
    *   *Tâche :* Créer une Route `/` + Contrôleur + Vue avec CSS natif (sans Service, sans Preline).
*   **N2 (Adapter) : Page Accueil "Pro"**
    *   *Tâche :* Intégrer **Preline UI** et passer au layout Blade.
    *   Intégration de couche Service
*   **🔴 Live Coding (Validation N2 > Vers N3)**
    *   *Challenge :* **Création de la page Détail Projet**.
    *   *Objectif :* Réaliser en direct une fonctionnalité clé du futur Mini-Projet N3 (brique manquante du N2).
*   **N3 (Transposer) : Mini-Projet Individuel "Portfolio Complet"**
    *   *Objectif :* Site complet (Home, Services, Projets, Contact) avec **Preline UI**.
    *   *Architecture :* Utilisation obligatoire de la couche **Service** (`PortfolioService`) pour fournir les données.
*   **🛑 Fin de Phase : Lancement Projet Fil Rouge (Solicode)**
    *   **Organisation :** Formation des équipes (Groupe 1, Groupe 2, Groupe 3).
    *   **Activité :** Présentation du "Blog Solicode", du Backlog Sprints, et initialisation du Git Flow par groupe.
    *   *Pas de développement de fonctionnalité Sprint ici, juste le setup Collaboratif.*

---

## 🗓️ Phase 3 : Données & Modélisation (Session S4)

**Thème :** Base de Données, Migrations, Eloquent ORM.

*   **N1 (Imiter) : Inventaire Simple**
    *   Créer une table `games` et la peupler via Factory.
*   **N2 (Adapter) + 🔴 Live Coding : Relations**
    *   *Tâche :* Créer une migration relationnelle (ex: `category_id`) et afficher les données liées.
    *   *Validation :* Comprendre `hasMany` / `belongsTo`.
*   **N3 (Transposer) : Mini-Projet Individuel "Blog [Ma Ville]" - Data**
    *   Créer la DB : `articles` (lieux/événements), `categories`.
    *   Connecter la Home Page pour afficher les articles réels de la BDD.
*   **🛑 Fin de Phase : SPRINT 1 (Visiteur)**
    *   **Rattrapage (Groupe) :** Finaliser le **Sprint 1** sur le **Projet Solicode** (Merge des features Visiteur, Recette).
    *   **Livrable :** Déploiement `sprint-1` sur serveur de test.

---

## 🗓️ Phase 4 : Back-Office & Gestion (Session S5)

**Thème :** CRUD, Formulaires, Validation.

*   **N1 (Imiter) : CRUD Basique**
    *   Controller Resource pour gérer une entité simple.
*   **N2 (Adapter) + 🔴 Live Coding : Upload & Validation**
    *   *Tâche :* Ajouter l'upload d'image et les règles de validation (Required, Min, etc.).
    *   *Validation :* Sécuriser un formulaire d'ajout.
*   **N3 (Transposer) : Mini-Projet Individuel "Blog [Ma Ville]" - Admin**
    *   Créer l'interface d'administration pour ajouter/modifier les lieux et événements de la ville.
*   **🛑 Fin de Phase : SPRINT 2 (Publication)**
    *   **Rattrapage (Groupe) :** Finaliser le **Sprint 2** sur le **Projet Solicode**.
    *   **Livrable :** Déploiement `sprint-2`.

---

## 🗓️ Phase 5 : Sécurité & Utilisateurs (Session S6)

**Thème :** Authentification, Rôles, Permissions.

*   **N1 (Imiter) : Login Simple**
    *   Utiliser Laravel Breeze/UI pour l'auth de base.
*   **N2 (Adapter) + 🔴 Live Coding : Middleware**
    *   *Tâche :* Protéger une route "/secret" accessible uniquement aux admins.
    *   *Validation :* Comprendre le cycle de vie d'une requête authentifiée.
*   **N3 (Transposer) : Mini-Projet Individuel "Blog [Ma Ville]" - Communauté**
    *   Permettre l'inscription des résidents.
    *   Ajouter les commentaires (Sprint 4 intégré ici).
*   **🛑 Fin de Phase : SPRINT 3 (Auth) & 4 (Commentaires)**
    *   **Rattrapage (Groupe) :** Intégrer Auth et Commentaires sur **Projet Solicode**.
    *   **Livrable :** Déploiement `sprint-4`.

---

## 🗓️ Phase 6 : Ouverture API (Session S7)

**Thème :** API REST, JSON Resources.

*   **N1 (Imiter) : API GET**
    *   Exposer une liste d'objets en JSON.
*   **N2 (Adapter) + 🔴 Live Coding : API Robuste**
    *   *Tâche :* Ajouter pagination, filtres et codes HTTP corrects (200, 201, 404).
    *   *Validation :* Tester l'API avec Postman/ThunderClient.
*   **N3 (Transposer) : Mini-Projet Individuel "Blog [Ma Ville]" - Open Data**
    *   Créer une API publique exposant les données touristiques de la ville.
*   **🛑 Fin de Phase : SPRINT 5 (API)**
    *   **Rattrapage (Groupe) :** Développer l'API du **Projet Solicode**.

---

## 🗓️ Phase 7 : Écosystème Mobile (Session S8)

**Thème :** Consommation API, Android Natif.

*   **N1 (Imiter) : Client HTTP**
    *   Utiliser Retrofit pour récupérer un JSON brut.
*   **N2 (Adapter) + 🔴 Live Coding : UI List**
    *   *Tâche :* Afficher les données JSON dans une RecyclerView/LazyColumn propre.
    *   *Validation :* Gérer le chargement et les erreurs réseau.
*   **N3 (Transposer) : Mini-Projet Individuel "App [Ma Ville]"**
    *   Créer l'application mobile compagnon du blog de ville.
*   **🛑 Fin de Phase : SPRINT 6 (Mobile) & CLÔTURE**
    *   **Rattrapage (Groupe) :** Finaliser l'app mobile **Projet Solicode**.
    *   **Livrable Final :** Démo complète (Web + Mobile) déployée.
