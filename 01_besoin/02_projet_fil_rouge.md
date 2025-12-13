---
title: "projet_fil_rouge.md"
version: "v3.0"
role: "Cahier des Charges Complet & Détaillé — Projet Fil Rouge"
related_to:
  - carte_techno_globale.md
  - versions-prototype.md
---

# 📌 Projet Fil Rouge : "Solicode News"

> **Vision** : Développer une plateforme éditoriale moderne (CMS) permettant la création, la gestion et la diffusion d'articles multi-canaux (Web & Mobile). Ce projet sert de colonne vertébrale pour valider l'ensemble des compétences Full Stack.

---

## 1. Contexte & Enjeux

### 1.1 Le Besoin Métier
Les organisations (Associations, Établissements de formation comme Solicode) ont besoin de communiquer sur leurs activités via un canal numérique centralisé et maîtrisé. Les réseaux sociaux ne suffisent plus : besoin de référencement, de structuration et d'une identité propre.

**La Solution :** Une plateforme de Blog dynamique, sécurisée et scalable, dotée d'une application mobile pour notifier les utilisateurs en temps réel.

### 1.2 Le Contexte Pédagogique
Ce projet n'est pas un simple exercice. Il est conçu pour simuler une **mission réelle en entreprise**.
*   **Contraintes Réelles :** Respect d'un cahier des charges, délais, qualité du code, sécurité.
*   **Technologies Imposées :** Stack moderne (Laravel 11, Tailwind, Kotlin/Compose).
*   **Double Cible :** 
    1.  **Version Groupe :** Déploiement interne pour l'école.
    2.  **Version Individuelle :** Adaptation pour un "client" réel (Association locale) pour valider le titre.

---

## 2. Description Fonctionnelle Détaillée

La plateforme se divise en 4 modules interconnectés.

### 🌐 Module 1 : Le Portail Web Public (Front-Office)
*L'interface visible par les visiteurs.*
*   **Page d'Accueil :** Mise en avant des articles récents ("À la une") et grille des derniers posts.
*   **Navigation :** Menu dynamique par **Catégories** (ex: Tech, Events, Tutos).
*   **Recherche Avancée :** Barre de recherche en temps réel (AJAX) filtrant par titre ou contenu.
*   **Lecture Immersive :** Page de détail d'un article avec :
    *   Image de couverture HD.
    *   Contenu riche (Markdown ou HTML).
    *   Auteur et Date de publication.
    *   Liste des **Tags** associés.
*   **Espace Social :** Zone de commentaires sous les articles (nécessite connexion).

### 🛠️ Module 2 : L'Administration (Back-Office)
*Le centre de contrôle sécurisé pour les gestionnaires.*
*   **Tableau de Bord (Dashboard) :** KPIs en temps réel (Nombre d'articles, Vues totales, Derniers inscrits).
*   **Gestion des Articles (Le Cœur) :**
    *   **Éditeur Riche :** WYSIWYG pour formater le texte.
    *   **Média Manager :** Upload et gestion des images associées.
    *   **Workflow de Publication :**
        *   *Brouillon* : Visible seulement par l'auteur.
        *   *En attente* : Soumis à validation.
        *   *Publié* : Visible sur le site public.
*   **Gestion des Taxonomies :** CRUD complet pour les Catégories et les Tags.
*   **Gestion des Utilisateurs :** 
    *   Liste des inscrits.
    *   Attribution des Rôles (Super Admin, Éditeur, Lecteur).
    *   Modération des commentaires.

### 🔌 Module 3 : API REST (Le Pont)
*L'interface d'échange de données.*
*   **Sécurité :** Authentification par Token (Sanctum).
*   **Diffusion :** Expose les articles, catégories et profils au format JSON standardisé.
*   **Performance :** Pagination des résultats et filtres optimisés.

### 📱 Module 4 : Application Mobile (Android)
*L'extension native pour la fidélisation.*
*   **Expérience Native :** Interface fluide développée en Kotlin / Jetpack Compose.
*   **Synchronisation :** Récupération des articles via l'API.
*   **Fonctionnalités Mobiles :**
    *   Login unifié (Même compte que le Web).
    *   Mise en **Favoris** locale ou synchronisée.
    *   Consultation optimisée pour petits écrans.

---

## 3. Acteurs & Rôles (Permissions)

Le système repose sur une gestion stricte des droits (RBAC) :


*   **Visiteur**
    *   *Accès :* Web Public (Oui), Mobile (Lecture), Admin (Non).
    *   *Droits :* Lecture seule.

*   **Membre**
    *   *Accès :* Web Public (Oui), Mobile (Oui), Admin (Non).
    *   *Droits :* Peut commenter, gérer ses favoris.

*   **Éditeur**
    *   *Accès :* Web Public (Oui), Mobile (Oui), Admin (Restreint).
    *   *Droits :* Crée/Édite **ses** articles. Ne peut pas publier directement (doit soumettre).

*   **Admin**
    *   *Accès :* Web Public (Oui), Mobile (Oui), Admin (Total).
    *   *Droits :* Valide/Publie les articles des autres. Gère utilisateurs et config.


---

## 4. Architecture Technique

*   **Backend :** Laravel 11.
*   **Architecture Logique :** N-Tiers. Les Contrôleurs ne contiennent pas de logique métier complexe (déléguée aux **Services**).
*   **Frontend Web :** Blade Components + Tailwind CSS (Preline UI).
*   **Base de Données :** MySQL 8.0.
*   **Mobile :** Android Natif (Kotlin, MVVM, Retrofit).

---

## 5. Livrables Attendus (Definition of Done)

Pour considérer le projet comme "Terminé", il doit inclure :
1.  **Code Source :** Dépôt Git propre avec historique (Commits conventionnels).
2.  **Base de Données :** Migrations et Seeders (Jeux de données de démo) fonctionnels.
3.  **Documentation :** README d'installation complet.
4.  **Déploiement :** Une URL accessible vers la version Web Production.
5.  **APK :** Le fichier d'installation de l'application mobile.
