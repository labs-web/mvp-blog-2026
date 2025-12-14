# 🔵 Sprint 4 : Commentaires & Communauté

## 📋 Pré-requis Pédagogiques
Ce Sprint est un moment de consolidation. Il n'y a pas de session théorique dédiée, c'est l'occasion de mettre en pratique l'autonomie.

## 1. 📝 Besoin
**Objectif :** Créer de l'engagement en permettant aux utilisateurs connectés de réagir aux articles.
*   Seuls les membres connectés peuvent commenter.
*   L'Admin doit pouvoir modérer (supprimer) tout commentaire inapproprié.

## 2. 🔍 Analyse
*   **Cas d'Utilisation (Use Cases) :**
    *   **Se connecter / S'inscrire** : Pré-requis pour commenter.
    *   **Poster un commentaire** : Via un formulaire en bas d'article (User).
    *   **Lire les commentaires** : Affichage sous l'article (Public).
    *   **Gérer les commentaires** : Valider ou Supprimer (Admin).
*   **Diagramme :** [sprint-04-commentaires.puml](sprint-04-commentaires.puml)

## 3. 🏗️ Conception
*   **Base de Données :**
    *   Table `comments` (`id`, `content`, `user_id`, `article_id`, `created_at`).
    *   **Relations :**
        *   `Article` hasMany `Comment`.
        *   `Comment` belongsTo `User`.
*   **Maquettage UI :**
    *   > [Voir Maquette Article (avec commentaires)](../../03_conception/maquettes-public/article.html)
    *   Section "Commentaires" en bas de `article.show`.
    *   Bouton "Supprimer" visible uniquement pour l'Admin (ou l'auteur du commentaire - *Bonus*).

