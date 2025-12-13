---
title: "projet_fil_rouge.md"
version: "v2.0"
role: "Cahier des Charges — Projet Fil Rouge (Web + API + Mobile)"
related_to:
  - carte_techno_globale.md
  - referentiel-competences.md
---

# 📌 Projet Fil Rouge — Plateforme Web & Mobile

> **Vision** : Une plateforme complète de gestion de contenus (type Blog), déclinée en Web (Admin/Public), API REST et Application Mobile.

## 1. Objectifs & Contexte d'usage
1.  **Technique** : Appliquer la stack définie dans `carte_techno_globale.md` (Laravel, Preline, API, Android Compose).
2.  **Pédagogique** : Servir de **colonne vertébrale** pour valider les compétences C1 à C7.
3.  **Livrable Multi-Contexte** : 
    *   **Contexte A (Groupe)** : Déployer le Blog pour le **Centre Solicode** (Travail collaboratif).
    *   **Contexte B (Individuel)** : Déployer une instance du Blog pour une **Association de Ville** (au choix de l'apprenant, ex: Tanger Culture), pour valider l'autonomie.

---

## 2. Découpage en Prototypes

Le projet est construit progressivement :

### P1 - Socle (N1 - Imiter)
**Description :** Une version **minimale (S0)** centrée sur les mécanismes de base.
*   **Objectif :** Acquérir le **strict minimum technique** (Web simple + API GET + Mobile Lecture) pour comprendre les interactions sans complexité métier.

### P2 - Prototype (N2 - Adapter)
**Description :** Une version **fonctionnelle, sécurisée et architecturée**, candidate au MVP.
*   **Objectif 1 :** Maîtriser toute la stack (Architecture N-Tiers, Spatie Permissions, API Complète).
*   **Objectif 2 :** Valider les acquis (via Live Coding) et minimiser les risques techniques avant le projet final.

### P3 - MVP (N3 - Transposer)
**Description :** La version **finale de Production** pour un client réel (Association).
*   **Objectif :** Transposer les acquis dans un contexte professionnel (Autonomie, Déploiement, Qualité).

---

## 3. Architecture Fonctionnelle

L'application s'articule autour de 4 blocs :

1.  **Web - Public (Front-Office)**
    *   Vitrine pour les visiteurs (Lecture seule).
    *   Liste d'articles, Recherche, Page détail.
    *   *Techno : Laravel Blade + Preline UI.*

2.  **Web - Admin (Back-Office)**
    *   Espace de gestion **sécurisé** (Authentification + Gestion des Rôles).
    *   **One Page CRUD** : Tableau de bord dynamique avec Recherche, Filtre, Pagination et CRUD sans rechargement de page (AJAX).
    *   *Techno : Laravel Blade + AJAX (Alpine.js optionnel) + Preline Admin Layouts + Spatie Permissions.*

3.  **API REST (Le Pont)**
    *   Interface de communication unique et **sécurisée**.
    *   Expose les données (JSON) au mobile et au front.
    *   *Techno : Laravel API Resource + Laravel Sanctum (Tokens).*

4.  **Couche Service (Core Métier)**
    *   **Architecture N-Tiers** : Centralise toute la logique métier (validation complexe, calculs, actions).
    *   Utilisée par les Contrôleurs Web et API pour éviter la duplication.
    *   *Techno : Classes de Service PHP (ex: ArticleService).*

5.  **Application Mobile**
    *   Consultation native sur Android.
    *   Synchronisation avec l'API.
    *   *Techno : Kotlin + Jetpack Compose.*

---

## 4. Acteurs & Rôles Cibles

*   **Visiteur :** Consulte le contenu public (Web/Mobile).
*   **Auteur :** Crée et édite ses propres contenus.
*   **Administrateur :** Gère toute la plateforme (Utilisateurs, Configuration).

---

## 5. Ancrage Compétences (C1-C7)

*   **C1 (Besoin)** : Maquettes HTML/CSS (Preline), diagrammes de cas d'usage.
*   **C2 (BDD)** : Schéma relationnel (Articles, Catégories, Users), Migrations.
*   **C3 (Back-end)** : Logique Laravel, Routes, Contrôleurs, API Resources.
    *   *Introduction N-Tiers :* Utilisation d'une **Couche Service** pour isoler la logique métier (Controller → Service → Model).
*   **C4 (Gestion)** : Git flow, Dépôt unique, Suivi par ticket.
*   **C5 (Mobile)** : App Android consommatrice d'API.
*   **C6 (Qualité)** : Tests unitaires, Jeux de données (Seeders).
*   **C7 (Déploiement)** : Mise en production sur serveur Linux.

> Ce fichier sert de **cahier des charges général** pour l'enseignant. Les spécifications techniques fines se trouvent dans les fichiers de prototypes respectifs.
