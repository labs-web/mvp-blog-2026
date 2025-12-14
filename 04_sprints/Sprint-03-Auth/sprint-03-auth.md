# 🟠 Sprint 3 : Authentification & Permissions

## 📋 Pré-requis Pédagogiques
Pour réussir ce Sprint, vous devez avoir validé la session de formation suivante :

### 🎓 Sessions de Formation
*   ✅ **Session S6 :** Authentification & Permissions (RBAC).
    *   *Acquis :* Sécurisation du **"Projet Ville"** (Espace Admin vs Espace Éditeur).

### 🔬 Labs & Veille
*   📚 **Veille Sécurité :** XSS, CSRF, et gestion des mots de passe.

## 1. 📝 Besoin
**Objectif :** Sécuriser l'application et définir qui peut faire quoi (Contrôle d'accès).
*   L'accès au Back-Office (`/admin`) doit être restreint.
*   Distinction claire entre :
    *   **Root :** A tous les pouvoirs.
    *   **Admin :** Gestion des utilisteurs et modération des articles. et les commentaires
    *   **Auteur :** Ne gère que ses propres articles.

## 2. 🔍 Analyse
*   **Cas d'Utilisation (Use Cases) :**
    *   **Se connecter** : Accès sécurisé (Login Form).
    *   **S'inscrire** : Création de compte (Register).
    *   **Gérer les rôles** : Attribution des droits (Admin).
    *   **Modérer** : Visibilité restreinte selon le rôle (Scope).
*   **Diagramme :** [sprint-03-auth.puml](sprint-03-auth.puml)

## 3. 🏗️ Conception
*   **Base de Données :**
    *   Table `users` (existante).
    *   **Rôles & Permissions :** Utilisation des tables du package `spatie/laravel-permission` (`roles`, `permissions`, `model_has_roles`).
*   **Maquettage UI :**
    *   > [Voir Maquettes Auth](../../03_conception/maquettes-auth/index.html)
    *   Pages : Login, Register, Forgot Password.

## 4. 💻 Réalisation (Tâches Techniques)
### ⚙️ Contraintes Techniques Critiques
*   **Sécurité :** Mots de passe hashés (Bcrypt/Argon2). Protection CSRF active.
*   **Package :** Utilisation de `spatie/laravel-permission` pour la gestion RBAC.
*   **Policies :** Logique d'autorisation dans des classes `Policy` (ex: `ArticlePolicy`), pas dans les contrôleurs.

### Tâches Détaillées
*   **Backend :**
    *   [ ] Installation `laravel/ui` ou `breeze` (Vue Auth).
    *   [ ] Installation `spatie/laravel-permission`.
    *   [ ] **Seeders :** Création des rôles `Admin` et `Author` + 1 SuperAdmin par défaut.
    *   [ ] `ArticlePolicy` : Définir `viewAny`, `update`, `delete`.
*   **Frontend :**
    *   [ ] Vues Login/Register stylisées avec **Preline UI**.
    *   [ ] Adaptation du Layout Admin : Afficher le nom de l'utilisateur connecté + Bouton Logout.
    *   [ ] Directives Blade : `@can`, `@role` pour masquer les boutons non autorisés.

## Indice de solution
(Policy Example)

```php
public function update(User $user, Article $article)
{
    // L'admin peut tout modifier, l'auteur seulement ses propres articles
    return $user->hasRole('admin') || $user->id === $article->user_id;
}
```
