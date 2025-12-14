---
title: "04_planning_pedagogique.md"
role: "Planning des Sessions de Formation (Phases et Sprints)"
---

# 🎓 Planning Pédagogique : Fil Rouge & Mini-Projets

Ce document structure la formation selon la stratégie de **Double Réalisation** :
1.  **Parcours Individuel (Formation)** : L'apprenant développe son propre projet ("Site de Ville / Association") via les niveaux N1/N2/N3.
2.  **Parcours Groupe (Production)** : En fin de phase, l'équipe consolide les acquis pour livrer le Sprint du "Projet Solicode".

---

## 🗓️ Phase 1 : Fondamentaux (S1-S2)

### Session S1 : Rappels PHP & Algorithmique (Imiter)
*   **Objectif :** Sécuriser les bases du langage sans framework.
*   **Contenu :** Variables, boucles, fonctions, manipulation de tableaux.

### Session S2 : Initiation Mobile (Android/Kotlin)
*   **Objectif :** Découverte de l'environnement Android Studio.
*   **Contenu :** Bases de Kotlin, "Hello World", Layouts simples.


<!-- TODO: ajouter une le description de travail à faire à la fin de la pahse, Présentation de programme de formation, les phase, session, travail individuel et travail en groupe -->
---


## 🗓️ Phase 2 : Sprint 1 : Visiteur


<!-- TODO : dans chaque phase , donner la description des session de chaque phase -->
### Session S3 Architecture MVC, Routing, Controller, Blade.

Dans cette session S3, on va pas suivre le Sprint1, on va trvailler su un site de type portifolio de projet.
car, nous vousslon commencer par la partie public et nous avvons pas encors les notions de base de données.

**Thème :** Architecture MVC, Routing, Controller, Blade.

*   **1️⃣ N1 (Imiter) : Page Accueil "Brute"**
    *   *Tâche :* Créer une Route `/` + Contrôleur + Vue avec CSS natif (sans Service, sans Preline).
    *   *Objectif :* Comprendre le cycle de vie `Request -> Route -> Controller -> View -> Response`.

*   **2️⃣ N2 (Adapter) : Page Accueil "Pro" (Prototype)**
    *   *Tâche :* Intégrer **Preline UI** et structurer avec Layout Blade (`app.blade.php`).
    *   *Architecture :* Introduction de la couche Service pour préparer les données.

*   **🧪 Live Coding (Validation N2 > Vers N3)**
    *   *Challenge :* **Création de la page "Détail Projet"**.
    *   *Objectif :* Coder en direct une route paramétrée (`/projets/{id}`) et sa vue (Brique manquante du N2).

*   **3️⃣ N3 (Transposer) : Création d'un portifolio**

---

### Session S4 : Base de Données, Migrations, Eloquent ORM.

Dans cette session, nous allons apprendre comment créer une base de données avec les deux de teste et de l'appliquer à notre projet file rouge


**Thème :** Base de Données, Migrations, Eloquent ORM.

*   **1️⃣ N1 (Imiter) : Inventaire Simple**
    *   Créer les Table Articles, Categories, Users qui couvre les trois type des relation avec Laravel
    *   Seeder
    *   Jeux de Teste.

<!-- TODO : il faut donner une description de N2 , puis le live coding deux étapes l'un aprés l'autre -->
<!-- TODO : ajouter cette information dans : 04_prompt.sprints.md  -->
*   **2️⃣ N2 (Adapter) + 🧪 Live Coding : Relations**
    *   Création des de test en utilisant les fichiers CSV
  
* Live coiding : Table Comment

*   **3️⃣ N3 (Transposer) : Projet Individuel  - Création de la base de données
    *   Création de tous les tables
    *   Avec les jeux de test


### Sprint 1

<!-- TODO : lire la description de sprint 1 de fichier : Sprint-01-Visiteur/README.md -->
*   **🛑 Fin de Phase : Créatpon de Sprint 1
    *   **Groupe (Solicode) :** Réalisation du **Sprint 1** (Page Accueil, Liste Articles, Détail).
    *   **Livrable :** Déploiement `sprint-1` (Version Visiteur fonctionnelle).

---



## 🗓️ Phase 2 : Sprint 2 : Back-Office & Gestion des articles sans sécurité


### Session S5 : CRUD, Formulaires, Validation.

**Thème :** CRUD, Formulaires, Validation.

*   **1️⃣ N1 (Imiter) : Gestion des articles :  CRUD Basique**
    *   Controller Resource standard pour gérer une entité simple.

*   **2️⃣ N2 (Adapter) + 🧪 Live Coding : Upload & Validation**
    *   *Tâche :* Ajouter l'upload d'image et les règles de validation (Required, Min).
    *   *Validation :* Sécuriser un formulaire d'ajout.
*  Live coding : filtrer par catégories

*   **3️⃣ N3 (Transposer) : Projet Individuel "Site Ville" - Admin**
    *   *Feature :* CRUD des articles avec lang, upload image, 
        *   Recherche, avec Ajax, 
  
  ### Sprint 2 : Gestion des articles  sans sécurité

*   **🛑 Fin de Phase : SPRINT 2 (Publication)**
    *   **Groupe (Solicode) :** Réalisation du **Sprint 2** (Gestion des Articles & Médias).
    *   **Livrable :** Déploiement `sprint-2`.

---

## 🗓️ Phase 3 : Sprint 3 : 

### Session S6 : Authentification, Rôles, Permissions.

**Thème :** Authentification, Rôles, Permissions.

*   **1️⃣ N1 (Imiter) : Login Simple**
    *   Utiliser Laravel UI/Breeze pour l'auth de base.
    *   Gestion des autorisation par Gate et Policy.

*   **2️⃣ N2 (Adapter) 
    *   Utilisation de spacité


*   ** 🧪 Live Coding : Middleware**

    * à déterminer 


*   **3️⃣ N3 (Transposer) : Projet Individuel "Site Ville"
    *   Crud Articles avec sécrutié, spacité, Role : Admin, Auteur

### Sprint 3 : Authentification, Rôles, Permissions.

à lire depuis : Sprint-03-Auth
---

## 🗓️ Phase 4 : Sprint 4 : Partie public - membre




## Phase 5 : Sprint 5 : API REST


### Session S7 : API REST, JSON Resources.

**Thème :** API REST, JSON Resources.

*   **1️⃣ N1 (Imiter) : API GET**
    *   Exposer une liste d'objets en JSON simple.

*   **2️⃣ N2 (Adapter) + 🧪 Live Coding : API Robuste**
    *   *Tâche :* Standards API (Codes HTTP 200/404, Pagination, Resource Class).
    *   *Validation :* Tester l'API avec Postman.

*   **3️⃣ N3 (Transposer) : Projet Individuel "Site Ville" - Open Data**
    *   *Feature :* Créer une API publique exposant les données touristiques pour les partenaires.
    *   *Livrable :* Endpoints API sécurisés (Sanctum).

*   **🛑 Fin de Phase : SPRINT 5 (API)**
    *   **Groupe (Solicode) :** Réalisation du **Sprint 5** (API Articles & Users).
    *   **Livrable :** Documentation API Swagger/Postman.

---

## 🗓️ Phase 6 : Sprint 6 : 

Session S8 : Écosystème Mobile (Session S8)


**Thème :** Consommation API, Android Natif (Kotlin).

*   **1️⃣ N1 (Imiter) : Client HTTP**
    *   Utiliser Retrofit pour récupérer un JSON brut.

*   **2️⃣ N2 (Adapter) + 🧪 Live Coding : UI List**
    *   *Tâche :* Afficher les données JSON dans une `LazyColumn` (Jetpack Compose).
    *   *Validation :* Gérer le chargement et les erreurs réseau.

*   **3️⃣ N3 (Transposer) : Projet Individuel "App Ville"**
    *   *Feature :* Application mobile compagnon affichant les actualités de la ville.
    *   *Livrable :* APK Android fonctionnel connecté à l'API personnelle.

