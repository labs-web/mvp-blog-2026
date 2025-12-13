---
title: "plan.md"
role: "Stratégie de Création des Maquettes (AI + Preline UI)"
---

# 🤖 Stratégie de Maquettage "Component-First"

Vous avez suggéré une approche **"Composants d'abord"** : créer des briques unitaires validées avant de construire les pages complètes.
**C'est une excellente méthode**, surtout avec l'IA. Elle garantit que toutes les pages auront le même style (cohérence) et facilite le travail de l'IA (assemblage plutôt que création pure).

Voici le plan détaillé et optimisé pour votre workflow :

---

## 1. L'Approche "Atomic Design" simplifiée
Au lieu de demander à l'IA de "générer une page d'accueil", nous allons procéder en deux temps :

1.  **Phase 1 : La Design Library (Composants)**
    *   Nous créons des fichiers HTML isolés pour chaque élément clé (ex: `components/header.html`, `components/card-article.html`).
    *   Nous les stylisons avec **Preline UI** et **Tailwind CSS**.
    *   **Validation :** Vous validez le look de ces briques individuellement.

2.  **Phase 2 : L'Assemblage (Pages)**
    *   Nous donnons ces fichiers de composants en *contexte* à l'IA.
    *   L'IA génère les pages (`index.html`, `dashboard.html`) en "copiant-collant" intelligemment ces blocs et en adaptant le contenu (textes, images).

### ✅ Pourquoi cette méthode est meilleure ?
*   **Cohérence Totale :** Le bouton "S'inscrire" sera identique partout.
*   **Moins d'erreurs :** L'IA n'invente pas du CSS, elle réutilise du code validé.
*   **Transition vers le Code (Blade/React) :** Ces fichiers composants deviendront directement vos Composants Blade (`<x-card-article />`) ou React plus tard.

---

## 2. Plan d'Action Concret

### Étape A : Structure du Projet
Nous allons organiser le dossier `maquettes-mvp` ainsi :

```text
maquettes-mvp/
├── components/           <-- "La Bibliothèque"
│   ├── layout-base.html  (Le squelette : <head>, CDN Tailwind/Preline, scripts)
│   ├── navbar.html
│   ├── footer.html
│   ├── card-article.html
│   ├── ui-button.html    (Différents états : primaire, secondaire...)
│   └── ui-input.html     (Champs formulaires standards)
│
├── index.html            <-- Pages finales (assemblage)
├── login.html
├── admin/
└── ...
```

### Étape B : Création des Composants (Ordre Prioritaire)
Nous allons créer ces fichiers un par un pour validation :

1.  **`layout-base.html`** : Pour configurer Tailwind CDN, Preline JS et la police (Inter ou autre).
2.  **`navbar.html`** et **`footer.html`** : La navigation responsive.
3.  **`card-article.html`** : L'élément central du site public.
4.  **`forms.html`** : Regroupant Input, Checkbox et Boutons.

### Étape C : Génération des Pages
Une fois les composants validés, le prompt pour l'IA sera simple :
> *"Utilise `layout-base.html` comme structure. Insère `navbar.html` en haut et `footer.html` en bas. Au centre, crée une grille de 3 colonnes utilisant `card-article.html` répété 6 fois avec des données fictives différentes."*

---

## 3. Outils Techniques
*   **Tailwind CSS (CDN)** : Pour le prototypage rapide sans build step.
    *   `<script src="https://cdn.tailwindcss.com"></script>`
*   **Preline UI** : Plugins et composants pré-faits.
    *   `<script src="https://cdn.jsdelivr.net/npm/preline/dist/preline.js"></script>`
*   **Images** : Utilisation de `https://placehold.co` ou `Unsplash` pour les placeholders.

---

## 🏁 Validation du Plan
Si ce plan vous convient, la prochaine instruction sera de **créer le dossier `components` et le fichier `layout-base.html`**.
