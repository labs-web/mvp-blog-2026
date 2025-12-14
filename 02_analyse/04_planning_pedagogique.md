---
title: "04_planning_pedagogique.md"
role: "Planning des Sessions de Formation (S1 à S8) & Méthode Imitation/Adaptation"
---

# 🎓 Planning Pédagogique (Méthode Imiter/Adapter/Transposer)

Ce document structure la progression des 8 Sessions de formation, en appliquant pour chaque étape technique la méthode pédagogique : **Imiter (N1)**, **Adapter (N2)**, **Transposer (MVP)**.

---

## 🗓️ Phase 1 : Fondamentaux (S1-S2)

### Session S1 : Rappels PHP & Algorithmique
*   **Objectif :** Sécuriser les réflexes PHP avant Laravel.
*   **Approche :**
    *   **N1 (Imiter)** : Script procédural simple (Variables, Boucles).
    *   **N2 (Adapter)** : Refactorisation en Fonctions / Classes simples.
    *   **MVP (Transposer)** : Petit squelette d'appli PHP sans framework.

### Session S2 : Initiation Mobile (Android/Kotlin)
*   **Objectif :** Découverte précoce de l'écosystème Android.
*   **Approche :**
    *   **N1 (Imiter)** : Installer Android Studio, "Hello World" avec une Liste statique.
    *   **N2 (Adapter)** : Modifier le design (Couleurs, Typo) et les données statiques.
    *   **MVP (Transposer)** : Créer une mini-app mobile autonome (ex: Catalogue events).

---

## 🗓️ Phase 2 : Développement Fil Rouge (S3-S8)

### Session S3 : Lancement Laravel (Interface Publique)
*   **Lien Sprint :** Sprint 1 (Socle & Lecture).
*   **Description :** Mise en place du MVC Laravel sans base de données (données simulées).
*   **Approche :**
    *   **N1 (Imiter)** : Route -> Contrôleur (Tableau PHP) -> Vue Blade.
    *   **N2 (Adapter)** : Modifier la vue (CSS, Badges) et la structure du tableau simulé.
    *   **MVP (Transposer)** : Concevoir une mini-interface publique pour un autre contexte.
*   **Proposition d'insertion :** *Démarrage du Sprint 1 technique en fin de session, avec initialisation du repository Git Flow.*

### Session S4 : Base de Données & Modèles
*   **Lien Sprint :** Sprint 1 (Suite - DB).
*   **Description :** Connexion MySQL, Migrations `artles`, `users` et Eloquent.
*   **Approche :**
    *   **N1 (Imiter)** : Configurer DB, migrer, afficher des articles "réels".
    *   **N2 (Adapter)** : Ajouter un champ en base (migration), mettre à jour la vue.
    *   **MVP (Transposer)** : Intégrer une nouvelle entité simple (ex: "Partenaires") au schéma.
*   **Proposition d'insertion :** *Finalisation du Sprint 1 (DB peuplée) et merge sur la branche develop.*

### Sprint 1 : 

aprés la réalisation de session S2 et S4, c'est te temps de finalider Sprint réalisation de la partie pubic : visiteur 

### Session S5 : Espace Admin & CRUD
*   **Lien Sprint :** Sprint 2 (Back-Office).
*   **Description :** Création et gestion des articles (Create, Read, Update, Delete).
*   **Approche :**
    *   **N1 (Imiter)** : CRUD standard (Resource Controller) simple.
    *   **N2 (Adapter)** : Améliorer les formulaires (Validation, UX).
    *   **MVP (Transposer)** : Créer un CRUD complet pour une autre entité (ex: Catégories).
*   **Proposition d'insertion :** *Lancement et clôture du Sprint 2 (Admin fonctionnel) durant cette session.*


### Sprint 2 : 

Réalisation de 


### Session S6 : Sécurité & Rôles
*   **Lien Sprint :** Sprint 3 (Sécurité).
*   **Description :** Authentification et Autorisations (Gates vs Spatie).
*   **Approche :**
    *   **N1 (Imiter)** : Auth Laravel UI + Gates simples (`is_admin`).
    *   **N2 (Adapter)** : Installation minimale de Spatie (Rôles `admin`/`auteur`).
    *   **MVP (Transposer)** : Configuration complète des rôles & permissions (Pro).
*   **Proposition d'insertion :** *Sprint 3 réalisé en itération : d'abord Auth simple, puis Refactoring avec Spatie.*

### Session S7 : API REST
*   **Lien Sprint :** Sprint 5 (API).
*   **Description :** Exposer les données du blog pour l'externe.
*   **Approche :**
    *   **N1 (Imiter)** : Endpoint GET simple (Liste/Détail).
    *   **N2 (Adapter)** : Ajout de filtres, pagination, formatage JSON uniforme.
    *   **MVP (Transposer)** : Conception d'une API complète documentée.
*   **Proposition d'insertion :** *Exécution du Sprint 5 en parallèle de la finalisation Web.*

### Session S8 : Application Mobile Connectée
*   **Lien Sprint :** Sprint 6 (Mobile).
*   **Description :** Consommation de l'API Laravel par l'app Android.
*   **Approche :**
    *   **N1 (Imiter)** : Appels HTTP (Retrofit) pour afficher la liste JSON.
    *   **N2 (Adapter)** : Gestion des états (Loading/Error), UI améliorée.
    *   **MVP (Transposer)** : App mobile complète et autonome consommant l'API.
*   **Proposition d'insertion :** *Sprint 6 clôturant le projet avec la démo de l'écosystème complet (Web + Mobile).*
