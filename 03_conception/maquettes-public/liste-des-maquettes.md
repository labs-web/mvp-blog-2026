---
title: "liste-des-maquettes.md"
role: "Liste des Maquettes à Réaliser pour le MVP"
---

# 🎨 Liste des Maquettes - MVP (Prototype N3)

Ce document recense l'ensemble des écrans à concevoir pour le MVP du projet "Fil Rouge".
L'objectif est de produire des maquettes fidèles aux contraintes techniques (Preline UI, Android Native) et fonctionnelles (MVP).

---

## 1. Web Public (Front-Office)
**Tech :** Blade, Tailwind CSS, Preline UI.
**Style :** Moderne, épuré, responsive mobile-first.

### 🏠 Pages Principales
*   **[WEB-01] Page d'Accueil (Home)** → `index.html`
    *   **Composants :** `navbar`, `hero`, `card-article`, `footer`.
    *   Header (Logo, Nav: Dev Web/Mobile/Design, Connexion/Inscription).
    *   Hero Section (Titre accrocheur, CTA vers inscription).
    *   Section "Derniers Articles" (Grille de cards).
    *   Section "Articles à la Une" (Carousel ou mise en avant).
    *   Footer (Liens légaux, copyright).

*   **[WEB-02] Page de Recherche / Liste des Articles** → `search.html`
    *   **Composants :** `navbar`, `search-bar`, `filters`, `card-article`, `pagination`, `footer`.
    *   Barre de recherche avec autocomplétion (visuel AJAX).
    *   Filtres latéraux ou supérieurs (Catégories, Tags).
    *   Grille de résultats avec pagination.
    *   État "Aucun résultat trouvé".

*   **[WEB-03] Page Détail Article** → `article.html`
    *   **Composants :** `navbar`, `article-detail`, `card-article` (similaires), `footer`.
    *   Image de couverture large.
    *   Titre, Auteur (Avatar + Nom), Date de publication.
    *   Corps de l'article (Rendu Markdown/HTML propre).
    *   Section "Articles similaires".
    *   (Optionnel) Section Commentaires.

### 🔐 Espace Authentification
### 🔐 Espace Authentification
*   **[WEB-04] Login** → `login.html` (Formulaire centré, lien mot de passe oublié).
    *   **Composants :** `layout-simple`, `auth-form`.
*   **[WEB-05] Register** → `register.html` (Nom, Email, Password, Confirmation).
    *   **Composants :** `layout-simple`, `auth-form`.

---

## 2. Web Admin (Back-Office)
**Tech :** Blade, Tailwind CSS, Layout Admin (Sidebar + Topbar).
**Style :** Fonctionnel, dense, orienté productivité.

### 📊 Dashboard & Global
### 📊 Dashboard & Global
*   **[ADM-01] Layout Admin** → `admin/layout.html` (ou intégré dans les autres pages)
    *   **Composants :** `admin-sidebar`, `admin-topbar`.
    *   Sidebar gauche (Menu : Dashboard, Articles, Catégories, Tags, Utilisateurs).
    *   Topbar (Fil d'ariane, Profil User, Logout).
*   **[ADM-02] Dashboard Home** → `admin/index.html`
    *   **Composants :** `admin-layout`, `stat-card`, `recent-table`.
    *   Cartes de statistiques (Nb Articles, Vues, Users).
    *   Tableau "Derniers inscrits" ou "Derniers articles publiés".

### 📝 Gestion des Contenus (CRUD Articles)
### 📝 Gestion des Contenus (CRUD Articles)
*   **[ADM-03] Liste des Articles (DataGrid)** → `admin/articles-list.html`
    *   **Composants :** `admin-layout`, `datatable`.
    *   Tableau colonnes : Titre, Auteur, Catégorie, Statut (Publié/Brouillon), Date.
    *   Actions par ligne : Voir, Modifier, Supprimer.
    *   Filtres en haut de liste.
*   **[ADM-04] Éditeur d'Article (Create/Edit)** → `admin/article-form.html`
    *   **Composants :** `admin-layout`, `form-elements`.
    *   Champs: Titre, Slug (auto), Catégorie (Select), Tags (Multi-select), Image (Upload).
    *   Zone de contenu (Grand Textarea ou intégré WYSIWYG style Markdown).
    *   Boutons d'action (Enregistrer brouillon, Publier).

### 🏷️ Gestion des Taxonomies
*   **[ADM-05] Gestion Catégories/Tags** → `admin/categories.html`
    *   Liste simple à gauche + Formulaire d'ajout/édition à droite (Split view) ou Modale.

### 👥 Gestion des Utilisateurs
*   **[ADM-06] Liste des Utilisateurs** → `admin/users.html`
    *   Tableau : Nom, Email, Rôle, Date inscription.
    *   Actions : Modifier Rôle, Bannir/Supprimer.

---

## 3. Application Mobile (Android)
**Tech :** Kotlin, Jetpack Compose.
**Style :** Material Design 3, Navigation native.

### 📱 Ecrans Principaux
*   **[MOB-01] Splash Screen** → `mobile/splash.html`
*   **[MOB-02] Login Screen** → `mobile/login.html`
*   **[MOB-03] Liste des Articles (Home)** → `mobile/home.html`
    *   TopAppBar (Titre, bouton Search).
    *   LazyColumn (Liste verticale des cards articles).
    *   Pull-to-refresh.
*   **[MOB-04] Détail Article** → `mobile/article.html`
    *   Image header (Collapsing Toolbar style).
    *   Contenu scrollable.
    *   FAB (Floating Action Button) pour favoris ou partage (Optionnel).
*   **[MOB-05] Profil Utilisateur** → `mobile/profile.html`
    *   Affichage infos user.
    *   Bouton Déconnexion.

---

## ✅ Checklist Qualité Maquettes
Pour chaque écran, valider :
*   [ ] Hiérarchie visuelle claire.
*   [ ] Contraste suffisant (Accessibilité).
*   [ ] États des boutons (Hover, Active, Disabled).
*   [ ] Champs de formulaire (Placeholder, Label, État Erreur).
*   [ ] Version Mobile du Web Public (Breakpoints).
