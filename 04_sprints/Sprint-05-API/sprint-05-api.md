# 🟣 Sprint 5 : API REST

## 📋 Pré-requis Pédagogiques
Pour réussir ce Sprint, vous devez avoir validé la session de formation suivante :

### 🎓 Sessions de Formation
*   ✅ **Session S7 :** Exposition des Données (API REST).
    *   *Acquis :* Création de l'API publique "Open Data" pour le Projet Ville.

### 🔬 Labs & Veille
*   🧪 **Lab API Resources :** Transformer les modèles Eloquent en JSON standardisé.
*   🧪 **Lab Sanctum :** Comprendre les tokens d'API.
*   📚 **Veille HTTP :** Codes de statut (200, 201, 401, 404, 500) et verbes (GET, POST).

## 1. 📝 Besoin
**Objectif :** Rendre les données du blog accessibles pour des applications tierces (notamment l'app Mobile du Sprint 6).
*   L'API doit retourner du JSON.
*   Certaines routes peuvent être publiques, d'autres protégées.

## 2. 🔍 Analyse
*   **Cas d'Utilisation (Use Cases) :**
    *   **Lister les articles (API)** : `GET /api/articles` (Avec pagination).
    *   **Détail article (API)** : `GET /api/articles/{id}`.
    *   **Connexion API** : `POST /api/login` (Retourne un Token).
*   **Diagramme :** [sprint-05-api.puml](sprint-05-api.puml)

## 3. 🏗️ Conception
*   **Endpoints :**
    *   Standard RESTful.
*   **Format de réponse :**
    *   `data` : Contient l'objet ou la liste.
    *   `meta` : (Optionnel) Pagination.

## 4. 💻 Réalisation (Tâches Techniques)
### ⚙️ Contraintes Techniques Critiques
*   **API Resources :** Ne JAMAIS retourner directement le Modèle Eloquent (`return Article::all()` ⛔). Utiliser `ArticleResource`.
*   **Gestion d'erreur :** Retourner un JSON propre même en cas d'erreur 404 (pas une page HTML Laravel).

### Tâches Détaillées
*   **Backend :**
    *   [ ] `php artisan install:api` (Laravel 11/12).
    *   [ ] `ArticleResource` : Définir les champs à exposer (id, titre, image_url, créateur).
    *   [ ] `Api/ArticleController` : Méthodes `index`, `show`.
    *   [ ] Route `login` pour générer un token Sanctum (pour tests futurs).
*   **Tests :**
    *   Tester avec **Postman**, **ThunderClient** ou **Insomnia**.

## Indice de solution
(Resource Example)

```php
public function toArray(Request $request): array
{
    return [
        'id' => $this->id,
        'title' => $this->title,
        'image' => asset('storage/' . $this->image_path),
        'author' => $this->user->name,
        'published_at' => $this->created_at->toIso8601String(),
    ];
}
```
