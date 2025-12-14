---
title: "03_sprint_backlog.md"
role: "Backlog Produit (Basé sur les Cas d'Utilisation)"
---

# 📅 Sprint Backlog Produit

Ce document définit le découpage technique du projet en **6 Sprints**.
Il référence directement les **Cas d'Utilisation (UC)** validés en phase d'analyse.

---

## 🟢 Sprint 1 : Lecture & Découverte
**Objectif :** Permettre aux visiteurs de découvrir et lire le contenu du blog.

### 🧩 Cas d'Utilisation (UC)
> [Voir Diagramme Visiteur](mvp/uc-mvp-visiteur.puml)
*   **UC_List** : Consulter la liste des articles (MVC basique).
*   **UC_Read** : Lire un article (Détail).

### ⚙️ Tâches Techniques
*   Setup Laravel 12 + Tailwind.
*   Modèles & Migrations : `User`, `Article`, `Category`, `Tag`.
*   Contrôleur `PublicController`.
*   Vues Blade : `home` (Grid), `article.show`.

---

## 🟡 Sprint 2 : Publication & Gestion des Contenus
**Objectif :** Offrir aux administrateurs un outil pour publier et gérer les articles.

### 🧩 Cas d'Utilisation (UC)
*   **UC_CRUD_Article** : Créer, Modifier, Supprimer un article (Backend).
*   **UC_Manage_Media** : Uploader une image de couverture.

### ⚙️ Tâches Techniques
*   Resource Controller : `ArticleController`.
*   Formulaires Blade (Create/Edit).
*   Storage Link (Images).

---

## 🟠 Sprint 3 : Authentification & Permissions
**Objectif :** Sécuriser l'accès et distinguer les droits entre Auteurs et Administrateurs.

### 🧩 Cas d'Utilisation (UC)
> [Voir Diagramme Membre](mvp/uc-mvp-membre.puml)
*   **UC_Login** : Se connecter (Admin/Auteur).
*   **UC_Register** : S'inscrire.
*   **UC_Moderate** : Modération (Admin peut tout voir, Auteur voit ses articles).

### ⚙️ Tâches Techniques
*   `laravel/ui` (Auth).
*   `spatie/laravel-permission` (Rôles).
*   Policies Laravel.

---

## 🔵 Sprint 4 : Commentaires & Communauté
**Objectif :** Fédérer une communauté en permettant les échanges et la modération.

### 🧩 Cas d'Utilisation (UC)
> [Voir Diagramme Membre](mvp/uc-mvp-membre.puml)
*   **UC_PostComment** : Poster un commentaire.
*   **UC_ReadComments** : Lire les commentaires d'un article.
*   **UC_ModerateComment** : Valider/Supprimer un commentaire (Admin).

### ⚙️ Tâches Techniques
*   Relation `Article` -> `Comment`.
*   Composant commentaire Blade.

---

## 🟣 Sprint 5 : API REST
**Objectif :** Exposition des données.

### 🧩 Cas d'Utilisation (UC)
*   **UC_API_List** : GET /api/articles.
*   **UC_API_Read** : GET /api/articles/{id}.
*   **UC_API_Auth** : Login via Token.

### ⚙️ Tâches Techniques
*   API Resources.
*   Laravel Sanctum.

---

## 📱 Sprint 6 : Application Mobile
**Objectif :** Client Android.

### 🧩 Cas d'Utilisation (UC)
*   **UC_Mobile_List** : Scroller le flux (via API).
*   **UC_Mobile_Read** : Lire natif.

### ⚙️ Tâches Techniques
*   Kotlin / Jetpack Compose.
*   Retrofit Client.
