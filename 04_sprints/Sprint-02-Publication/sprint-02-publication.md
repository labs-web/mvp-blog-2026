# 🟡 Sprint 2 : Publication (Back-Office sans Auth)

## 📋 Pré-requis Pédagogiques
Pour réussir ce Sprint, vous devez avoir validé la session de formation suivante :

### 🎓 Sessions de Formation
*   ✅ **Session S5 :** CRUD, Formulaires & Validation.
    *   *Acquis :* Création du **"Back-Office Ville"** (Gestionnaire de Lieux et Événements).

### 🔬 Labs & Veille
*   🧪 **Lab Upload :** Gérer l'upload de fichiers avec Laravel (`Storage`).

## 1. 📝 Besoin
**Objectif :** Offrir une interface d'administration pour gérer le contenu du blog (Articles).
*   *Note Importante :* Ce Sprint se focalise sur la **fonctionnalité** (CRUD). La sécurité (Login) sera ajoutée au Sprint 3.
*   L'interface est accessible publiquement pour l'instant (ex: `/admin/articles`).

## 2. 🔍 Analyse
*   **Cas d'Utilisation (Use Cases) :**
    *   **Gérer les articles** : Créer, Éditer, Supprimer.
    *   **Uploader des médias** : Ajouter une image de couverture.
    *   **Soumettre pour validation** : Proposer un article (Auteur).
    *   **Valider et Publier** : Rendre public (Admin).
    *   **Rechercher et Filtrer** : Trouver facilement un contenu.
*   **Diagramme :** [sprint-02-publication.puml](sprint-02-publication.puml)


## 3. 🏗️ Conception
*   **Maquettage UI :**
    *   > [Voir Maquettes Admin](../../03_conception/maquettes-admin/index.html)
    *   **Pages clés :** Liste Articles (Tableau), Formulaire Création/Édition.
## 4. 💻 Réalisation (Tâches Techniques)

### ⚙️ Contraintes Techniques Critiques
*   **Internationalisation (Lang) :** Toutes les chaînes de caractères (labels, messages validation, statuts) doivent être gérées via les fichiers de traduction Laravel (`lang/fr/*.php`). Pas de texte en dur.
*   **Architecture :** Utilisation stricte de la **Couche Service** (`ArticleService`) pour la logique métier (Upload, Sauvegarde). Le Contrôleur ne fait que valider et répondre.
*   **UX Dynamique :** La recherche et les filtres dans le tableau des articles doivent être réalisés en **AJAX** (sans rechargement de page) ou avec Livewire/Alpine.js.

### Tâches Détaillées
*   **Backend :**
    *   [ ] `ArticleController` (Resource Controller).
    *   [ ] `ArticleRequest` (Validation stricte).
    *   [ ] `ArticleService` (Business Logic).
    *   [ ] **API Interne :** Endpoint ou méthode pour le filtrage AJAX.
*   **Frontend (Preline UI) :**
    *   [ ] **Layout Admin :** Création de `layouts/admin.blade.php` spécifique (Sidebar, Header, Slot content).
    *   [ ] **Vue Index :** Tableau des articles avec :
        *   Barre de recherche (AJAX).
        *   Filtre par Catégorie (AJAX).
        *   Pagination.
    *   [ ] **Vue Form :** Création/Édition avec gestion des erreurs de validation (i18n).
