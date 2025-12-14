# 🟣 Sprint 5 : API REST

## 📋 Pré-requis Pédagogiques
Pour réussir ce Sprint, vous devez avoir validé la session de formation suivante :

### 🎓 Sessions de Formation
*   ✅ **Session S7 :** Exposition des Données (API REST).
    *   *Acquis :* Création de l'API publique "Open Data" pour le Projet Ville.

### 🔬 Labs & Veille
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
