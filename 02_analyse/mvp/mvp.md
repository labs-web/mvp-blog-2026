---
title: "mvp-n3.md"
version: "v1.3"
role: "Cahier des Charges Simplifié — MVP (Niveau N3)"
---

# 🚀 Le Projet MVP en Bref

> **Objectif Simple :** Créer un **Blog Professionnel** complet où l'on peut lire des articles sur le web et sur mobile, et les gérer via une interface d'administration sécurisée.

---

## 1. 🌍 Partie Publique (Le Site Web)
*C'est la vitrine visible par tout le monde.*

*   **Lecture Agréable :** Une page d'accueil moderne affichant les derniers articles.
*   **Recherche Rapide :** Une barre de recherche pour trouver un article instantanément sans recharger la page.
*   **Navigation Facile :** Trier les articles par **Catégorie** (ex: Tech, Sport) ou par **Sujet** (Tags).
*   **Interaction :** Lire un article complet et **laisser un commentaire**.

## 2. 🔐 Partie Administration (Le Back-Office)
*C'est le poste de pilotage, accessible uniquement par connexion.*

*   **Tableau de Bord :** Vue d'ensemble simple (Combien d'articles ? Combien de vues ?).
*   **Rédaction Puissante :** Un éditeur de texte complet (comme Word) pour écrire les articles et **ajouter des images**.
*   **Workflow de Publication (Le circuit de validation) :**
    1.  Un **Rédacteur** écrit un brouillon.
    2.  L'article est mis "En attente".
    3.  L'**Admin** relit, valide et publie l'article pour qu'il soit visible.
*   **Gestion Totale :** Créer, modifier ou supprimer des utilisateurs, des catégories et des tags.

## 3. 📱 Partie Mobile (L'Application Android)
*C'est la version de poche pour les lecteurs.*

*   **Compte Unifié :** On se connecte avec le même compte que sur le site web.
*   **Lecture Native :** Une interface fluide adaptée au téléphone pour lire les articles.


---

## ✅ Scénario de fin (La Preuve que ça marche)
Pour valider le projet, tu devras jouer les 4 séquences suivantes sans bug :

### 1. ✍️ Création d'un article (Auteur)
1.  Je me connecte en tant qu'**Auteur**.
2.  Dans mon Dashboard, je clique sur "Nouvel Article".
3.  Je remplis le formulaire : Titre, Image à la une, Contenu, et je choisis une Catégorie.
4.  Je clique sur "Enregistrer".
5.  *Résultat :* L'article apparaît dans ma liste avec le badge `En attente`. Il n'est **pas** visible sur le site public.

### 2. 👮 Validation (Admin)
1.  Je me connecte en tant qu'**Administrateur**.
2.  Je vois une notification ou un badge sur "Articles en attente".
3.  J'ouvre l'article de l'Auteur, je le relis.
4.  Je change son statut de `En attente` à `Publié`.
5.  *Résultat :* L'article est maintenant visible sur le site web Public.

### 3. 💬 Commentaire (Membre)
1.  Je vais sur le site public (Front-Office) et je me connecte en tant que **Membre**.
2.  Je clique sur l'article fraîchement publié.
3.  En bas de page, j'écris un commentaire : *"Super article !"* et je valide.
4.  *Résultat :* Mon commentaire s'affiche (ou apparaît "en attente de modération" selon configuration).

### 4. 🛡️ Modération (Admin)
1.  Retour sur l'interface **Admin**.
2.  Je vais dans la section "Commentaires".
3.  Je vois le dernier commentaire posté.
4.  Je peux le **Supprimer** ou le **Valider**.
5.  *Résultat :* Si supprimé, il disparaît immédiatement du site public et mobile.
