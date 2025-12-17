---
title: "05_organisation/methodologie_cascade.md"
role: "Référentiel Méthodologique : Le Modèle en Cascade (Théorie & Pratique)"
version: "v7.0"
---

# 🌊 Le Modèle en Cascade (Waterfall)

Ce document explore le cycle de vie logiciel sous 5 angles : sa théorie exacte, ses adaptations (Web, Objet, Moderne) et son application pratique pour l'apprenant.

---

## 1. 📜 La Méthode Exacte (Théorie W. Royce)

Le modèle historique se découpe en phases séquentielles strictes.

1.  **Exigences Système (System Requirements)**
    *   *Définition :* Les exigences font l'objet d'une expression des besoins. C'est la définition globale du système.
    *   *Livrable :* Étude de faisabilité.
2.  **Analyse (Analysis)**
    *   *Définition :* Spécification des fonctions.
    *   *Livrable :* Cahier des Charges Fonctionnel.
3.  **Conception (Design)**
    *   *Définition :* Définition de l'architecture.
    *   *Livrable :* Dossier de Conception Technique.
4.  **Codage (Coding)**
    *   *Définition :* Programmation.
    *   *Livrable :* Code Source.
5.  **Tests (Testing)**
    *   *Définition :* Validation.
    *   *Livrable :* Rapport de Recette.
6.  **Opérations (Operations)**
    *   *Définition :* Maintenance.
    *   *Livrable :* Manuel Utilisateur.

---

## 2. 🌐 Application aux Projets Web

Dans le développement Web, les phases s'adaptent pour traiter la séparation Front/Back.

1.  **Analyse :** Arborescence du site (Sitemap), User Flow (Parcours utilisateur).
2.  **Conception :**
    *   *Visuelle :* Wireframes (Zoning) -> Maquettes UI (Figma).
    *   *Données :* Schéma Relationnel (MLD/SQL).
3.  **Réalisation :**
    *   *Intégration :* HTML/CSS (Transformation de la maquette).
    *   *Développement Back :* API, Logique serveur.
4.  **Déploiement :** Hébergement, Nom de domaine, HTTPS.

---

## 3. 🧩 Application à la Conception Orientée Objet (COO)

Si le projet utilise un langage Objet (Java, PHP Laravel, Kotlin), la phase de **Conception** est critique pour ne pas produire du "code spaghetti".

1.  **Analyse :** Identification des Acteurs et des Cas d'Utilisation (Use Case Diagram).
2.  **Conception Statique :**
    *   Identification des **Classes** (Entités métier).
    *   Définition des Attributs et Méthodes.
    *   *Livrable :* **Diagramme de Classes UML**.
3.  **Conception Dynamique :**
    *   Comment les objets "discutent" entre eux ?
    *   *Livrable :* **Diagramme de Séquence**.
4.  **Implémentation :** Traduction directe du diagramme en Classes ( `class Article { ... }` ).

---

## 4. 🚀 Application Moderne (Vision 2025)

Comment ces termes anciens se traduisent dans une stack technique moderne (Cloud, Agile, DevOps).

*   **Requirements** ➡️ **Infrastructure & Cadrage** (Choix Cloud, AWS/Azure).
*   **Analyse** ➡️ **Product Management** (User Stories, Jira Backlog).
*   **Conception** ➡️ **Architecture & Design System** (Composants UI réutilisables).
*   **Codage** ➡️ **Implémentation Clean Code** (PR, Code Review).
*   **Tests** ➡️ **QA & CI** (Tests Automatisés Cypress/PHPUnit).
*   **Opérations** ➡️ **DevOps & CI/CD** (Déploiement continu Docker/K8s).

---

## 5. 🎓 Proposition Pratique : La "Micro-Cascade" (L'Apprenant)

Voici comment l'apprenant doit appliquer rigoureusement ce cycle pour **une seule fonctionnalité** (ex: "Créer un Article").

### Étape A : Analyse (Je comprends)
*   **Quoi faire :** Lire le ticket/besoin.
*   **Livrable :** Un petit **Diagramme de Cas d'Utilisation** (Acteur -> Action).

### Étape B : Conception (Je dessine)
*   **Quoi faire :**
    1.  **UI :** Dessiner la **Maquette** exacte de l'écran (Formulaire).
    2.  **Objet :** Dessiner le **Diagramme de Classes** (Quelle classe Service ? Quelle méthode `create()` ? Quels paramètres ?).
    3.  **Données :** Vérifier la table BDD.
*   **Livrable :** Maquette validée + Schéma UML.

### Étape C : Réalisation (Je code)
*   **Quoi faire :**
    1.  Créer la Migration (BDD).
    2.  Coder la Classe Service (Logique).
    3.  Coder le Contrôleur et la Vue.
*   **Livrable :** Code fonctionnel poussé sur Git.

### Étape D : Validation (Je vérifie)
*   **Quoi faire :** Tester que l'article se crée bien.
*   **Livrable :** Démo fonctionnelle.

> **Règle d'or :** Interdiction de coder (C) si la Conception (B) n'est pas claire.
