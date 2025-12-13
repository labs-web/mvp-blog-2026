---
title: "components.md"
role: "Liste des Composants à Créer (Design System)"
---

# 🧩 Liste des Composants HTML (MVP)

Cette liste définit les briques unitaires qui seront assemblées pour créer les pages.
Chaque fichier doit être créé dans le dossier `maquettes-mvp/components/`.

---

## 🏗️ Structure & Layouts
Ces fichiers définissent l'enveloppe globale.

*   **`layout-base.html`**
    *   Squelette HTML5 (`<!DOCTYPE html>`).
    *   Inclusion des CDN (Tailwind CSS, Preline UI, Google Fonts).
    *   Variables CSS de base (Couleurs).
*   **`layout-simple.html`** (Pour Login/Register)
    *   Variante épurée sans header/footer complexe, fond coloré ou image.
*   **`admin-layout.html`** (Combine Sidebar + Topbar)
    *   Structure spécifique Dashboard (Sidebar fixe à gauche, Topbar en haut, Contenu fluide).

---

## 🧭 Navigation
*   **`navbar.html`** (Web Public)
    *   Logo, Liens navigation, Boutons Connexion/Inscription (ou Menu User si connecté).
    *   Responsive (Menu burger sur mobile).
*   **`footer.html`** (Web Public)
    *   Colonnes de liens, Copyright, Réseaux sociaux.
*   **`admin-sidebar.html`** (Back-Office)
    *   Logo Admin, Menu vertical (Dashboard, Articles, etc.), Liens actifs.
*   **`admin-topbar.html`** (Back-Office)
    *   Fil d'ariane (Breadcrumb), Recherche locale, Dropdown Profil.

---

## 🪪 Cartes & Affichage Contenu
*   **`hero.html`**
    *   Grande section d'intro (Titre, Sous-titre, CTA).
*   **`card-article.html`**
    *   Format "Grid Item" : Image, Catégorie (Badge), Titre, Extrait, Auteur, Date.
*   **`stat-card.html`** (Admin)
    *   Icône, Chiffre clé, Libellé, Tendance (+/- %).
*   **`article-detail.html`** (Contenu sans le layout autour)
    *   Header article (Titre H1, Meta), Image principale, Corps de texte typographié (Prose).

---

## 🔍 Recherche & Filtres
*   **`search-bar.html`**
    *   Champ de recherche large avec icône loupe.
*   **`filters.html`**
    *   Sidebar ou Toolbar pour filtrer par Catégorie/Tag.
*   **`pagination.html`**
    *   Liens Précédent/Suivant, Numéros de page.

---

## 📝 Formulaires & Tables
*   **`auth-form.html`** (Base Login/Register)
    *   Champs Email/Password stylisés, Bouton Submit, "Mot de passe oublié".
*   **`form-elements.html`** (Collection)
    *   Input text, Textarea, Select, Checkbox, Toggle Switch, File Upload.
*   **`datatable.html`** (Admin)
    *   Tableau complet avec En-têtes, Lignes zébrées, Actions (Edit/Delete), Statut coloré.

---

## 🔄 États Vides & Feedback
*   **`empty-state.html`**
    *   Illustration SVG simple + Texte "Aucun résultat" + Bouton retour.
*   **`modal-confirm.html`**
    *   Modale pour confirmer la suppression (Overlay, Titre, Boutons Annuler/Confirmer).
