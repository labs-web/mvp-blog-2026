# 🧩 Inventaire des Composants Admin (Design System)

**Stack :** Tailwind CSS + Preline UI + Lucide Icons.

---

## 1. Structure (Layout)

### A. Sidebar (`components/sidebar.html`)
Barre latérale fixe à gauche.
*   **Logo :** Haut.
*   **Navigation :** Liens avec état actif/inactif (Dashboard, Articles, Catégories, Tags, Utilisateurs).
*   **Icônes :** Lucide Icons (`layout-dashboard`, `file-text`, `layers`, `tag`, `users`).
*   **Mobile :** DOIT être responsive (Offcanvas `hs-overlay`).

### B. Navbar (`components/navbar.html`)
Barre supérieure.
*   **Toggle Mobile :** Bouton hamburger pour ouvrir la sidebar.
*   **Breadcrumb :** Fil d'ariane contextuel.
*   **User Menu :** Dropdown avec Avatar + Nom -> "Profil", "Déconnexion".

---

## 2. Affichage de Données

### C. KPI Card (`components/kpi-card.html`)
Utilisé sur le Dashboard.
*   **Contenu :** Titre, Valeur (Gros), Icône (Coin supérieur droit), Variation (Optionnel).
*   **Style :** Fond blanc, ombre légère, bordure fine.

### D. Tableau de Données (`components/table.html`)
Pour toutes les listes (Articles, Users, etc.).
*   **Header :** Gris clair, texte majuscule petit.
*   **Lignes :** Hover effect.
*   **Actions :** Boutons Éditer/Supprimer en fin de ligne (ou menu contextuel).

### E. Status Badge (`components/badge.html`)
Pour les états (Publié/Brouillon) et Rôles.
*   **Style :** Pillule arrondie.
*   **Couleurs :**
    *   Vert (Success) : Publié, Admin.
    *   Gris (Neutral) : Brouillon, User.
    *   Rouge (Danger) : Archivé.
    *   Bleu (Info) : Auteur.

---

## 3. Interactif

### F. Modale (`components/modal.html`)
Pour la confirmation de suppression, édition rapide de catégorie/rôle.
*   **Library :** `Preline UI Modal`.
*   **Structure :** Header (Titre + X), Body, Footer (Annuler / Confirmer).

### G. Composants de Formulaire
*   **Input Standard :** Bordure grise, focus ring bleu, label au dessus.
*   **Toggle Switch :** Pour "Is Featured".
*   **Select :** Pour "Catégorie" ou "Rôle".
