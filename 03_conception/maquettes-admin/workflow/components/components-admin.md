
# Liste des Composants Génériques (Admin)

Ce document recense les composants réutilisables pour l'interface d'administration. Ils doivent être intégrés dans `maquettes-admin/components/`.

## 1. Structure (Layout)

*   **`layout/sidebar.html`** : Navigation principale à gauche.
    *   Responsive (Offcanvas mobile).
    *   Liens : Dashboard, Articles, Catégories, Tags, Utilisateurs.
    *   Icônes : Lucide.
*   **`layout/navbar.html`** : Barre supérieure (Header).
    *   Bouton toggle Sidebar.
    *   Barre de recherche.
    *   Menu Profil (Dropdown).

## 2. Affichage de Données (Data Display)

*   **`data/kpi-card.html`** : Carte indicateur (Dashboard).
    *   Titre, Valeur, Icône, Variation (Trending).
    *   Tooltip d'info.
*   **`data/table.html`** : Tableau générique complet.
    *   Header avec Titre et Bouton d'action.
    *   Colonnes avec Checkbox.
    *   Menu d'actions (Dropdown) en fin de ligne.
*   **`data/status-badge.html`** : Badges d'état/rôle.
    *   Variantes couleur : Succès, Info, Danger, Neutre.
    *   Forme arrondie (Pill).

## 4. Formulaires & Saisie

*   **`forms/input-group.html`** : Champ de saisie standard.
    *   Label, Input, Message d'aide/erreur.
*   **`forms/file-upload.html`** : Zone d'upload d'image (Drag & Drop).
    *   Aperçu de l'image sélectionnée.
*   **`forms/rich-editor.html`** : Éditeur de texte riche (WYSIWYG simplifié).
    *   Toolbar (Gras, Italique, Liste, Lien).
    *   Zone de contenu.
*   **`forms/select.html`** : Menu déroulant natif ou custom.

## 5. Interactif & Feedback

*   **`feedback/modal.html`** : Fenêtre modale générique.
    *   Titre, Corps, Footer (Fermer/Action).
    *   Basée sur `hs-overlay` (Preline).
*   **`feedback/alert.html`** : Messages de notification.
    *   Succès, Erreur, Info.

## 6. Widgets Complexes

*   **`widgets/recent-articles.html`** : Tableau simplifié "Derniers Articles" (Dashboard).
    *   Liste compacte.
    *   Statut et Date.
*   **`widgets/activity-list.html`** : Liste des activités récentes (Dashboard Auteur).
    *   "Vous avez publié..."
    *   "Nouveau commentaire sur..."

---

## Directives de Design (Tailwind & Preline)
*   Utiliser **Preline UI** pour les composants interactifs (Dropdowns, Modals).
*   Couleurs : Garder la palette `blue-600` comme primaire.
*   Typographie : `Inter` pour le corps, `Outfit` pour les titres.
*   Dark Mode : Prévoir les classes `dark:...` dès le début.
