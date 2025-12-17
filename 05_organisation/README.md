---
title: "05_organisation/README.md"
role: "Guide d'Organisation & Workflow de Groupe"
version: "v2.0"
---

# 🤝 Guide d'Organisation : Groupe Lead Dev

Ce document définit la méthodologie de travail pour le groupe de production ("Groupe Lead Dev").\
L'objectif est de simuler un environnement professionnel rigoureux où chaque membre monte en compétence sur toutes les phases du cycle de vie logiciel.

---

## 1. 🎯 Objectifs Pédagogiques

Tous les membres du groupe doivent valider les compétences techniques et méthodologiques suivantes :

1.  **Analyse du Besoin** : Comprendre et découper le projet.
2.  **Analyse Technique & Labs** : Identifier et maîtriser les pré-requis (ex: Ajax).
3.  **Conception** :
    *   Diagrammes de Cas d'Utilisation (Use Cases).
    *   Maquettage UI/UX (Validation client).
    *   Diagrammes de Classes (Validation architecture).
4.  **Réalisation** : Développement propre, tests et BDD.

---

## 2. 📂 Stratégie Git & Branches

L'organisation du dépôt suit un modèle Git Flow strict pour garantir la stabilité du code.

### 2.1 Les Branches Principales

| Branche     | Description                                                              |
| :---------- | :----------------------------------------------------------------------- |
| **main**    | Code de production, stable et validé. Déployé sur le serveur final.      |
| **develop** | Branche d'intégration. Tous les développements validés y sont fusionnés. |

### 2.2 Les Branches Individuelles (Feature Branches)

Chaque apprenant travaille sur sa propre branche nommée selon le format : `prenom.nom` (ex: `madani.ali`).

Cette branche doit contenir une structure de dossiers normalisée pour documenter l'avancement :

```text
/ (Racine de la branche prenom.nom)
│
├── 01_fonctionnalite/     # Cas d'utilisation à développer
├── 02_labs/               # Exercices et prototypes techniques
├── 03_maquette/           # Maquettes et comptes-rendus validation
├── 04_realisation/        # Code source, DB scripts, Tests
└── README.md              # Journal de bord de la tâche
```

---

## 3. 📝 Le Journal de Bord Individuel (`README.md`)

À la racine de votre branche individuelle, le fichier `README.md` doit toujours être à jour. Il sert de tableau de bord pour le Lead Dev (Formateur).

**Structure type du README.md :**

```markdown
# Journal de Bord : [Votre Nom]

## 🛠 Résumé du Travail
- **Fonctionnalité** : [Nom du module, ex: Gestion Commentaires]
- **État** : [En cours / Validé / Bloqué]

## 🧪 1. Labs Techniques
Liste des concepts techniques validés avant de commencer :
- [x] Lab Ajax request
- [ ] Lab Gestion des fichiers PHP

## 🎨 2. Maquettes & Validation
- Lien vers les maquettes : [Lien]
- **Validation Client** : 
    - Date : [JJ/MM/AAAA]
    - Acteurs présents : [Noms]
    - Remarques : [Liste des retours]

## 🏗 3. Conception & Réalisation
- Classe Services identifiées : [Liste des méthodes]
- Base de données : [Tables ajoutées/modifiées]
- Jeux de tests réalisés : [Scénarios]
```

---

## 4. 🔄 Workflow Détaillé par Phase

### Phase 1 : Labs (Mise à niveau)
Si des lacunes techniques sont identifiées lors de l'analyse (ex: "Je ne sais pas faire un appel Ajax"), un **Lab** doit être créé.
*   **Règle :** Aucun développement ne commence tant que les Labs associés ne sont pas maitrisés.

### Phase 2 : Fonctionnalité & Maquettage
1.  **Use Cases :** Isoler le diagramme de cas d'utilisation spécifique à la tâche.
2.  **Maquette :** Produire la maquette exacte à développer.
3.  **Validation Utilisateur :**
    *   Organiser une séance de validation avec les acteurs (Visiteur, Membre, Admin, Auteur, Formateur).
    *   Rédiger un compte-rendu incluant la date, les participants et les validations.

### Phase 3 : Réalisation & Services
L'objectif est de produire un code propre et maintenable.

1.  **Base de Données :** Création des migrations et des **Jeux de Données** (Seeders) pour tester.
2.  **Service Layer :**
    *   Avant de coder, définir l'interface du Service (méthodes, entrées/sorties).
    *   **Diagramme de Classe Dynamique :** Si plusieurs membres travaillent sur des services liés, le premier à démarrer propose une architecture (méthodes publiques) que les autres devront respecter.
3.  **Tests :** Validation unitaire des méthodes du service.

---

## 5. ✅ Definition of Done (DoD)

Une tâche est considérée comme **Terminée** quand :
1.  Les Labs sont validés.
2.  La maquette est validée par un "Client".
3.  Le code est mergé sur `develop` via une Pull Request.
4.  Les tests (manuels ou automatisés) sont passants.
