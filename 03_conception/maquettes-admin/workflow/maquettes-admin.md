# Liste et Spécifications des Maquettes Admin

### 🔐 Login Admin (`./index.html`)
Page de connexion sécurisée.
*   **Objectif :** Authentification des administrateurs et auteurs.
*   **Composants clés :** Formulaire Login.

### 📊 Dashboard Admin (`./dashboard-admin.html`)
Vue d'ensemble globale.
*   **Objectif :** Pilotage de la plateforme.
*   **Contenu :** KPIs globaux, Derniers articles, Modération.

### 📈 Dashboard Auteur (`./dashboard-auteur.html`)
Espace personnel.
*   **Objectif :** Suivi de ma production.
*   **Contenu :** Mes KPIs, Accès rapide "Écrire", Mes brouillons.

### 3. Gestion des Contenus

#### A. Articles
*   **Liste :** `articles/index.html` (Tableau, Filtres, Actions de masse)
*   **Formulaire :** `articles/form.html` (Édition/Création, Upload Image, Rich Text)
*   **Specs :** [specs/articles.md](specs/articles.md)

#### B. Catégories
*   **Liste & Actions :** `categories/index.html`
*   **Specs :** [specs/categories.md](specs/categories.md)

#### C. Tags
*   **Liste & Actions :** `tags/index.html`
*   **Specs :** [specs/tags.md](specs/tags.md)

### 📝 Articles - Liste (`./articles/index.html`)
Gestion du contenu.
*   **Objectif :** Lister, filtrer et gérer les statuts des articles.
*   **Composants clés :** Tableau de données avec filtres avancés.

### ✍️ Articles - Formulaire (`./articles/form.html`)
Éditeur de contenu.
*   **Objectif :** Création et modification complète d'un article.
*   **Composants clés :** Éditeur riche (WYSIWYG), Sidebar de publication.

### 🏷️ Catégories (`./categories/index.html`)
Gestion de la structure.
*   **Objectif :** CRUD hiérarchique des catégories.
*   **Composants clés :** Liste simple + Modale d'édition.

### #️⃣ Tags (`./tags/index.html`)
Gestion des mots-clés.
*   **Objectif :** CRUD simple des étiquettes.
*   **Composants clés :** Liste simple + Modale d'édition.

### 👥 Utilisateurs (`./utilisateurs/index.html`)
Gestion des membres.
*   **Objectif :** Liste des inscrits et modération.
*   **Action clé :** Attribution des Rôles (Admin/Auteur).


# 📂 Architecture des Dossiers

Ce document valide la structure des fichiers à créer pour la Phase 1, en respectant la convention `kebab-case`.

## Arborescence

```bash
maquettes-admin/
│
├── index.html              # 🔐 Connexion 
├── dashboard-admin.html    # 📊 Dashboard Administrateur
├── dashboard-auteur.html   # 📊 Dashboard Auteur
│
├── articles/               # 📝 Gestion Articles
│   ├── index.html          # Liste des articles
│   └── form.html           # Création / Édition
│
├── categories/             # 🏷️ Gestion Catégories
│   └── index.html          # Liste + Modale
│
├── tags/                   # #️⃣ Gestion Tags
│   └── index.html          # Liste + Modale
│
├── utilisateurs/           # 👥 Gestion Utilisateurs
│   └── index.html          # Liste + Modale Rôle
│
└── assets/                 # Ressources statiques
    ├── css/
    │   └── style.css       # Styles personnalisés (si besoin)
    ├── js/
    │   └── script.js       # Scripts globaux
    └── img/
        └── logo.svg        # Logos et placeholders
```

## Conventions
*   **Dossiers :** Pluriel (`articles`, `categories`).
*   **Fichiers Liste :** Toujours `index.html`.
*   **Fichiers Formulaire :** `form.html` (ou `create.html`/`edit.html` si distincts, mais ici unifié).
*   **Noms :** Tout en minuscule, séparé par des tirets (`kebab-case`).
