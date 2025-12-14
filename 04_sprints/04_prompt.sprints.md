---
title: "04_prompt.sprints.md"
role: "Guide de Conception des Mini-Projets Pédagogiques (N1/N2/N3)"
---

# 🎓 Guide de Conception Pédagogique (N1 / N2 / N3)

Ce document définit la philosophie de création des exercices et mini-projets pour les apprenants. L'objectif est une montée en compétence **progressive** et **sécurisée**.

---

## 🏗️ Structure Standard d'une Session

Chaque session technique doit suivre strictement cette progression en 3 temps :

### 1️⃣ Niveau 1 (Imiter) : "Les Fondations Brutes"
*   **Objectif :** Comprendre le fonctionnement natif du Framework ou du Langage.
*   **Contraintes Techniques :**
    *   ⛔ **Pas de librairie externe** (Pas de UI Kit, pas de packages complexes).
    *   ⛔ **Pas d'architecture avancée** (Pas de Service, code direct dans le Controller/Main).
    *   ✅ **Focus :** Syntaxe pure, Flux de données basique (MVC simple).
*   **Exemple S3 :** Page Accueil avec CSS natif, Route simple, Contrôleur qui retourne un String ou une vue basique.

### 2️⃣ Niveau 2 (Adapter) : "Vers le Professionnalisme"
*   **Objectif :** Intégrer les outils de productivité et les standards (Prototype).
*   **Contraintes Techniques :**
    *   ✅ **Introduction des Librairies :** Installation de **Preline UI** / Tailwind.
    *   ✅ **Introduction de l'Architecture :** Début de structuration (Layouts Blade, Composants).
    *   🚀 **Rôle :** C'est le **Prototype** technique qui valide la faisabilité avant le grand projet.
*   **Exemple S3 :** Refonte de la Page Accueil avec Preline UI, découpage en Layout `app.blade.php`.

### 🧪 Live Coding (Validation N2 > Vers N3)
*   **Objectif :** Réaliser en direct une fonctionnalité clé du futur Mini-Projet N3 (brique manquante du N2).
*   **Format :** Un défi (45 min) consistant à développer une fonctionnalité réelle du Mini-Projet (ex: "Page Détail").

### 3️⃣ Niveau 3 (Transposer) : "L'Architecture Complète (Version Individuelle)"
*   **Objectif :** Développer individuellement la fonctionnalité du Sprint en respectant l'architecture cible.
*   **Alignement (La Double Réalisation) :** 
    *   Le projet Fil Rouge se construit dans deux contextes distincts.
    *   **Contexte Formation (Individuel) :** L'apprenant développe ici version du projet Fil Rouge ("Association d'une ville") en suivant les exigences du N3.
    *   **Contexte Établissement (Groupe) :** En fin de phase (Sprint), les apprenants regrouperont leurs compétences pour refaire/finaliser la version officielle installée au centre.
    *   *Note :* L'apprenant développe donc l'application **deux fois** (Entraînement Individuel -> Production Groupe).
*   **Contraintes Techniques :**
    *   ✅ **Architecture Stricte Obligatoire :** Utilisation de la **Couche Service**.
    *   🏆 **Livrable :** Le module fonctionnel du Sprint (ex: Gestion des Articles), fonctionnel et complet.
*   **Exemple S3 :** Développement complet du module "Publication Article" avec `ArticleService` (Version Perso).

---

## 🎯 Relation N1 / N2 / N3

1.  **N1** valide la **Compréhension** ("Je sais comment ça marche sous le capot").
2.  **N2** valide l'**Outillage** ("Je sais utiliser les outils modernes pour aller vite").
3.  **N3** valide l'**Architecture** ("Je sais construire une application maintenable et scalable").
