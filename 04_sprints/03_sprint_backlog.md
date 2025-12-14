---
title: "03_sprint_backlog.md"
role: "Backlog Produit (Basé sur les Cas d'Utilisation)"
---

# 📅 Sprint Backlog Produit

Ce document définit le découpage technique du projet en **6 Sprints**.
Il référence directement les **Cas d'Utilisation (UC)** validés en phase d'analyse.

---

## 🟢 Sprint 1 : Visiteur & Découverte
**Objectif :** Permettre aux visiteurs de découvrir et lire le contenu du blog.
> [Voir Détails Sprint](./Sprint-01-Visiteur/Sprint-01-Visiteur.md)

### 🧩 Cas d'Utilisation (UC)
> [Voir Diagramme Visiteur](./Sprint-01-Visiteur/sprint-01-visiteur.puml)
*   **Lister les articles** : Affichage grille des articles (MVC basique).
*   **Lire un article** : Page détail article.
*   **Rechercher** : Recherche dynamique (AJAX).
*   **Filtrer** : Filtrage par Catégorie/Tag.

### ⚙️ Tâches Techniques
*   Setup Laravel 12 + Tailwind + **Preline UI**.
*   Modèles & Migrations : `User`, `Article`, `Category`, `Tag`.
*   Contrôleur `PublicController` + **Service Layer** (`ArticleService`).
*   Vues Blade : `home` (Grid), `article.show`.
*   **AJAX** : Recherche instantanée.

---

## 🟡 Sprint 2 : Publication (Back-Office sans Auth)
**Objectif :** Offrir une interface de gestion des contenus (CRUD) pour aborder les formulaires sans la complexité de sécurité.
> [Voir Détails Sprint](./Sprint-02-Publication/sprint-02-publication.md)

### 🧩 Cas d'Utilisation (UC)
> [Voir Diagramme Publication](./Sprint-02-Publication/sprint-02-publication.puml)
*   **Gérer les articles** : Créer, Modifier, Supprimer un article.
*   **Uploader des médias** : Ajouter une image de couverture.
*   **Soumettre / Publier** : Workflow de validation basique.
*   **Rechercher & Filtrer** : UX dynamique (AJAX) sur le tableau de bord.

### ⚙️ Tâches Techniques
*   Resource Controller : `ArticleController`.
*   **Service Layer** : Logique métier (Upload, Sauvegarde).
*   **i18n** : Textes et messages de validation via fichiers de langue.
*   **Layout Admin** : Structure spécifique (`layouts/admin.blade.php`).
*   **AJAX** : Filtres et Recherche dynamique sur le tableau de bord.

---

## 🟠 Sprint 3 : Authentification & Rôles
**Objectif :** Sécuriser l'accès et distinguer les droits entre Auteurs et Administrateurs.
> [Voir Détails Sprint](./Sprint-03-Auth/sprint-03-auth.md)

### 🧩 Cas d'Utilisation (UC)
> [Voir Diagramme Auth](./Sprint-03-Auth/sprint-03-auth.puml)
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
> [Voir Détails Sprint](./Sprint-04-Commentaires/sprint-04-commentaires.md)

### 🧩 Cas d'Utilisation (UC)
> [Voir Diagramme Commentaires](./Sprint-04-Commentaires/sprint-04-commentaires.puml)
*   **UC_PostComment** : Poster un commentaire.
*   **UC_ReadComments** : Lire les commentaires d'un article.
*   **UC_ModerateComment** : Valider/Supprimer un commentaire (Admin).

### ⚙️ Tâches Techniques
*   Relation `Article` -> `Comment`.
*   Composant commentaire Blade.

---

## 🟣 Sprint 5 : API REST
**Objectif :** Exposition des données.
> [Voir Détails Sprint](./Sprint-05-API/sprint-05-api.md)

### 🧩 Cas d'Utilisation (UC)
> [Voir Diagramme API](./Sprint-05-API/sprint-05-api.puml)
*   **UC_API_List** : GET /api/articles.
*   **UC_API_Read** : GET /api/articles/{id}.
*   **UC_API_Auth** : Login via Token.

### ⚙️ Tâches Techniques
*   API Resources.
*   Laravel Sanctum.

---

## 📱 Sprint 6 : Application Mobile
**Objectif :** Client Android.
> [Voir Détails Sprint](./Sprint-06-Mobile/sprint-06-mobile.md)

### 🧩 Cas d'Utilisation (UC)
> [Voir Diagramme Mobile](./Sprint-06-Mobile/sprint-06-mobile.puml)
*   **UC_Mobile_List** : Scroller le flux (via API).
*   **UC_Mobile_Read** : Lire natif.

### ⚙️ Tâches Techniques
*   Kotlin / Jetpack Compose.
*   Retrofit Client.
