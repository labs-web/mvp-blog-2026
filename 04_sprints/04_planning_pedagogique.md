---
title: "04_planning_pedagogique.md"
role: "Planning des Sessions de Formation (Phases et Sprints)"
---

# 🎓 Planning Pédagogique : Fil Rouge & Mini-Projets

Ce document structure la formation selon la stratégie de **Double Réalisation** :
1.  **Parcours Individuel (Formation)** : L'apprenant développe son propre projet **"Site de Ville / Association"** (ou Portfolio pour S3) pour acquérir les compétences.
2.  **Parcours Groupe (Production)** : En fin de phase, l'équipe consolide les acquis pour livrer le Sprint du **"Projet Solicode"**.

---

## 🗓️ Phase 1 : Fondamentaux (S1-S2)

### Session S1 : Rappels PHP & Algorithmique (Imiter)
*   **Objectif :** Sécuriser les bases du langage sans framework.
*   **Contenu :** Variables, boucles, fonctions, manipulation de tableaux.

### Session S2 : Initiation Mobile (Android/Kotlin)
*   **Objectif :** Découverte de l'environnement Android Studio.
*   **Contenu :** Bases de Kotlin, "Hello World", Layouts simples.

> **📌 Bilan Phase 1 :** Présentation du programme annuel, du **Projet Fil Rouge Solicode** (Travail Groupe) et du **Projet Ville/Association** (Travail Individuel).

---

## 🗓️ Phase 2 : Sprint 1 - Visiteur & Découverte

Cette phase se concentre sur la partie publique du site.

### Session S3 : Architecture MVC & Rendu (Portfolio)
> *Note : Dans cette session, nous travaillons sur un "Portfolio" statique car nous n'abordons pas encore la base de données.*

*   **1️⃣ N1 (Imiter) : Page Accueil "Brute"**
    *   *Tâche :* Route `/` + Contrôleur + Vue CSS natif.
    *   *Objectif :* Comprendre le cycle MVC `Request -> Response`.
*   **2️⃣ N2 (Adapter) : Page Accueil "Pro" (Preline)**
    *   *Tâche :* Intégration **Preline UI** + Layouts Blade (`app.blade.php`).
    *   *Architecture :* Introduction de la couche Service (Données statiques).
*   **🧪 Live Coding : Page Détail**
    *   *Challenge :* Créer une route paramétrée `/projets/{id}`.
*   **3️⃣ N3 (Transposer) : Projet "Portfolio Personnel"**
    *   *Livrable :* Site complet (Home, Services, Projets, Contact) utilisant Preline UI & Services.

### Session S4 : Données & Modélisation (Projet Ville)
*   **1️⃣ N1 (Imiter) : Modélisation Base**
    *   *Tâche :* Créer Migrations/Models pour `Articles`, `Categories`, `Users`.
    *   *Data :* Seeders avec Factory.
*   **2️⃣ N2 (Adapter) : Relations & Tests CSV**
    *   *Tâche :* Peupler la base via un fichier CSV réel (Jeux de tests).
    *   *Architecture :* Relations `belongsTo`, `hasMany`.
*   **🧪 Live Coding : Table Relationnelle**
    *   *Challenge :* Implémenter la table `Comments` et ses relations.
*   **3️⃣ N3 (Transposer) : Projet "Site Ville" - Socle Data**
    *   *Livrable :* Création de la BDD complète du projet Ville avec jeux de données réalistes.

> **🛑 Fin de Phase (Sprint 1) :** Réalisation en Groupe du **Sprint 1 Solicode** (Sprint 1 - Visiteur & Découverte).

---

## 🗓️ Phase 3 : Sprint 2 (Back-Office sans Sécurité)

### Session S5 : CRUD & Gestion des Articles
*   **1️⃣ N1 (Imiter) : CRUD Basique**
    *   *Tâche :* Resource Controller pour créer/éditer un article simple.
*   **2️⃣ N2 (Adapter) : Validation & Upload**
    *   *Tâche :* Upload Image, Règles de validation (Request), Messages d'erreur.
*   **🧪 Live Coding : Filtres**
    *   *Challenge :* Filtrer la liste des articles par Catégorie.
*   **3️⃣ N3 (Transposer) : Projet "Site Ville" - Admin**
    *   *Livrable :* Back-office complet pour gérer Lieux/Actualités (Upload, Validation, Recherche AJAX).
    *   lang 

> **🛑 Fin de Phase (Sprint 2) :** Réalisation en Groupe du **Sprint 2 Solicode** (Sprint 2 : Publication (Back-Office sans Auth)).

---

## 🗓️ Phase 4 : Sprint 3 (Sécurité & Auth)

### Session S6 : Authentification & Permissions
*   **1️⃣ N1 (Imiter) : Login Standard**
    *   *Tâche :* Install Laravel UI + Gate/Policy de base.
*   **2️⃣ N2 (Adapter) : Rôles Avancés (Spatie)**
    *   *Tâche :* Implémentation de `spatie/laravel-permission`. Distinction Admin/Auteur.
*   **🧪 Live Coding : Middleware Custom**
    *   *Challenge :* Créer un Middleware pour protéger l'accès `/admin`.
*   **3️⃣ N3 (Transposer) : Projet "Site Ville" - Accès**
    *   *Livrable :* Sécurisation du Back-office (Admin seulement) et Espace Éditeur.

> **🛑 Fin de Phase (Sprint 3) :** Réalisation en Groupe du **Sprint 3 Solicode** (Sprint 3 : Authentification & Rôles).

---

## 🗓️ Phase 5 : Sprint 4 (Communauté & Membres)


pas de session seulement le développement de Sprint 4

> **� Fin de Phase (Sprint 4) :** Réalisation en Groupe du **Sprint 4 : Commentaires & Communauté**.

---

## 🗓️ Phase 6 : Sprint 5 (API REST)

### Session S7 : Exposition des Données
*   **1️⃣ N1 (Imiter) : API Simple**
    *   *Tâche :* Endpoint GET `/api/articles`.
*   **2️⃣ N2 (Adapter) : API Standardisée**
    *   *Tâche :* API Resources, Codes HTTP, Pagination.
*   **3️⃣ N3 (Transposer) : Projet "Site Ville" - Open Data**
    *   *Livrable :* API publique des Lieux touristiques (Sécurisée Sanctum).

> **🛑 Fin de Phase (Sprint 5) :** Réalisation en Groupe du **Sprint 5 : API REST**.

---

## 🗓️ Phase 7 : Sprint 6 (Mobile)

### Session S8 : Application Android
*   **1️⃣ N1 (Imiter) : Appel Réseau**
    *   *Tâche :* Retrofit Simple Call.
*   **2️⃣ N2 (Adapter) : Liste Dynamique**
    *   *Tâche :* RecyclerView/LazyColumn avec images (Coil/Glide).
*   **3️⃣ N3 (Transposer) : App "Ville Compagnon"**
    *   *Livrable :* App Mobile affichant les news de la ville.


Sprint 6 : Mobile : Sprint 6 : Application Mobile


## Phase 8 : 🛑 Clôture du Projet :** Livraison Finale **Web + Mobile** du Projet Solicode.
