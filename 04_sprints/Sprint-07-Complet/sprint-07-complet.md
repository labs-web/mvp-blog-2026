# 🛠️ Sprint-07-Complet : Administration Complète

## 📋 Pré-requis Pédagogiques
Pour réussir ce Sprint, vous devez avoir validé les sessions de formation suivantes :

### 🎓 Sessions de Formation
*   ✅ **Session Back-End :** API REST & Sécurité.
    *   *Acquis :* Authentification, autorisation, gestion des rôles.
*   ✅ **Session Front-End / Admin :** Interfaces de gestion (CRUD).

### 🔬 Labs & Veille
*   📚 **Veille Sécurité :** Gestion des rôles et permissions (RBAC).
*   📚 **Veille UX Admin :** Interfaces d’administration efficaces.

---

## 1. 📝 Besoin
**Objectif :** Mettre en place une interface d’administration complète permettant à un **Administrateur** de gérer les données fonctionnelles et les utilisateurs de l’application.

*   L’administration est réservée aux utilisateurs disposant d’un rôle spécifique.
*   Elle permet le pilotage global du contenu et des accès.

---

## 2. 🔍 Analyse
### 👤 Acteur
*   **Administrateur**

### 📌 Cas d’Utilisation (Use Cases)
*   **Gérer les Catégories**
    *   Créer, modifier, supprimer des catégories.
*   **Gérer les Tags**
    *   Ajouter, éditer, supprimer des tags.
*   **Gérer les Utilisateurs**
    *   Créer, modifier, désactiver des comptes utilisateurs.
*   **Attribuer un Rôle**
    *   Définir les droits d’un utilisateur.

### 🔗 Relations
*   L’attribution d’un rôle est une **extension** de la gestion des utilisateurs.

### 📐 Diagramme
*   **Diagramme de cas d’utilisation :**  
    [sprint-07-complet.puml](sprint-07-complet.puml)

---

## 3. 🏗️ Conception
### 🧱 Architecture
*   **Type :** Back-office / Administration sécurisée
*   **Principe :** Accès restreint par rôle
*   **Organisation :**
    *   Gestion centralisée des entités (catégories, tags, utilisateurs)
    *   Séparation claire entre fonctionnalités métier et sécurité

---

## 4. ✅ Critères de Validation
*   L’administrateur peut gérer catégories, tags et utilisateurs.
*   Les rôles sont correctement attribués et appliqués.
*   Les accès sont sécurisés et limités selon le rôle.
*   L’interface est claire et adaptée à un usage administratif.
