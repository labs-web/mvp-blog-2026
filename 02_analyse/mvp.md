---
title: "mvp-n3.md"
version: "v1.2"
role: "Cahier des Charges Détaillé — MVP (Niveau N3 - Transposer)"
reads_after: ["projet_fil_rouge.md", "carte_techno_globale.md", "prototype-n2.md"]
---

# 🚀 Prototype N3 — Le MVP (Produit Minimum Viable)

> **Phase :** Transposer (Production).
> **Contexte :** Le code ne doit plus être un "exercice" mais un **produit livrable** pour un client réel (Association).

---

## 1. Périmètre Fonctionnel Global

Le MVP reprend toutes les bases du N2 et les finalise pour la production. Il doit être **robuste**, **sécurisé** et **agréable à utiliser**.

### 1.1 Web Public (Front-Office)
*   **Design :** Interface soignée avec **Preline UI** (Responsive parfait).
*   **Fonctionnalités :**
    *   Accueil dynamique (Derniers articles, articles à la une).
    *   Recherche textuelle performante (AJAX).
    *   Filtrage par Catégorie et par Tag.
    *   Page Détail riche (Image, Auteur, Date, Contenu Markdown ou HTML rendu).
    *   Système de commentaires simples.

### 1.2 Web Admin (Back-Office)
*   **Architecture :** One Page CRUD (Expérience fluide sans rechargement).
*   **Dashboard :** Statistiques simples (Nombre d'articles, vues, derniers inscrits).
*   **Gestion des Contenus (Articles) :**
    *   Éditeur de texte riche (WYSIWYG).
    *   **Upload d'images**.
    *   Gestion des statuts (Brouillon / Publié / Archivé).
*   **Gestion des Taxonomies :** CRUD Catégories et Tags.
*   **Sécurité & Accès :**
    *   Gestion des Utilisateurs.
    *   Attribution des Rôles (Admin, Auteur) via **Spatie Permissions**.
    *   **Workflow de Validation :** L'Auteur crée l'article (Statut "En attente"), l'Admin le valide (Statut "Publié").

### 1.3 API REST (Backend)
*   **Sécurité :** Authentification Full via **Laravel Sanctum** (pour l'app mobile).
*   **Endpoints :**
    *   Auth (Login, Logout, Me).
    *   Articles (Liste paginée, Filtres, Détail).
    *   Favoris (Toggle like/bookmark).
*   **Performance :** Utilisation des API Resources pour formater le JSON proprement.

### 1.4 Application Mobile (Android Natif)
*   **Stack :** Kotlin + Jetpack Compose + Retrofit + Coil (Images).
*   **Fonctionnalités :**
    *   **Authentification :** Écran de Login (Connexion via API Sanctum).
    *   **Navigation :** Bottom Navigation Bar (Accueil, Recherche, Favoris, Profil).
    *   **Offline First (Intro) :** Mise en cache simple des données (Room ou Retrofit Cache) pour consultation sans internet.
    *   **Interactions :** Ajouter aux favoris (Synchronisé avec le serveur).

---

## 2. Critères de Qualité (Definition of Done)

Pour valider le N3/MVP, le projet doit respecter :

1.  **Code Clean :** Architecture N-Tiers respectée (Controller -> Service -> Model).
2.  **Sécurité :** Pas de failles évidentes (XSS, CSRF géré par Laravel), Mots de passe hashés, API sécurisée.
3.  **Expérience Utilisateur (UX) :** Pas d'erreurs 500 visibles, messages d'erreurs clairs, chargements (Loaders) visibles lors des requêtes AJAX/API.
4.  **Déploiement :** L'application Web est accessible en ligne (HTTPS) sur un serveur de production (VPS ou Hébergement mutualisé).

---

## 3. Scénario de Démonstration (Jury)

L'apprenant devra jouer ce scénario sans bug :

1.  **Auteur :** Je me connecte, je rédige un article avec photo, je le soumets.
2.  **Admin :** Je reçois l'article "En attente", je le relis et je le **Publie**.
3.  **Web Public :** L'article apparaît. Je laisse un commentaire.
4.  **Mobile :** J'ouvre l'app, je consulte l'article et je vois le commentaire synchronisé.

---

## 4. Diagramme de Cas d'Utilisation

Voir le détail dans le fichier dédié : [Diagramme de Cas d'Utilisation](mvp-n3-usecases.md)
