# 🔵 Sprint 4 : Commentaires & Communauté

## 📋 Pré-requis Pédagogiques
Ce Sprint est un moment de consolidation. Il n'y a pas de session théorique dédiée, c'est l'occasion de mettre en pratique l'autonomie.

### 🎓 Sessions de Formation
*   🚫 **Pas de Session spécifique.**
    *   *Mode :* Travail en autonomie ou en Peer Programming.
    *   *Objectif :* Réinvestir les acquis MVC (Contrôleur, Modèle, Vue) et Relations (HasMany).

## 1. 📝 Besoin
**Objectif :** Créer de l'engagement en permettant aux utilisateurs connectés de réagir aux articles.
*   Seuls les membres connectés peuvent commenter.
*   L'Admin doit pouvoir modérer (supprimer) tout commentaire inapproprié.

## 2. 🔍 Analyse
*   **Cas d'Utilisation (Use Cases) :**
    *   **Poster un commentaire** : Via un formulaire en bas d'article (User).
    *   **Lire les commentaires** : Affichage sous l'article (Public).
    *   **Modérer** : Supprimer un commentaire abusif (Admin).
*   **Diagramme :** [sprint-04-commentaires.puml](sprint-04-commentaires.puml)

## 3. 🏗️ Conception
*   **Base de Données :**
    *   Table `comments` (`id`, `content`, `user_id`, `article_id`, `created_at`).
    *   **Relations :**
        *   `Article` hasMany `Comment`.
        *   `Comment` belongsTo `User`.
*   **Maquettage UI :**
    *   Section "Commentaires" en bas de `article.show`.
    *   Bouton "Supprimer" visible uniquement pour l'Admin (ou l'auteur du commentaire - *Bonus*).

## 4. 💻 Réalisation (Tâches Techniques)
### ⚙️ Contraintes Techniques Critiques
*   **Composants Blade :** Utiliser `<x-comment-item :comment="$comment" />` pour éviter de dupliquer le code HTML.
*   **Sécurité :** Validation du formulaire (contenu non vide).

### Tâches Détaillées
*   **Backend :**
    *   [ ] Migration `create_comments_table`.
    *   [ ] Modèle `Comment` avec relations.
    *   [ ] `CommentController` (store, destroy).
*   **Frontend :**
    *   [ ] Formulaire d'ajout (visible si `@auth`).
    *   [ ] Liste des commentaires (boucle `@foreach`).
    *   [ ] Feedback utilisateur ("Commentaire ajouté !").

## Indice de solution
(Blade Component usage)

```html
<div class="mt-8">
    <h3>Commentaires ({{ $article->comments_count }})</h3>
    @foreach($article->comments as $comment)
        <x-comment-item :comment="$comment" />
    @endforeach
</div>
```
