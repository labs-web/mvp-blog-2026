## 🔹 Version 1 — Rappel PHP (sans Prototype)

### N1 — Imiter

**Description**
Les apprenants refont des **exercices guidés** de base en PHP : variables, tableaux, fonctions, inclusion de fichiers, mini-POO (classe simple).
On reste sur de **petits scripts isolés**, sans framework.

**Objectif pédagogique N1**
Sécuriser les **réflexes de base en PHP** pour que la syntaxe ne soit plus un frein quand on bascule sur Laravel.

### N2 — Adapter

**Description**
À partir de scripts PHP fournis (mal structurés, répétitifs), les apprenants doivent :

* **réorganiser** le code (fonctions, petites classes),
* **séparer** la logique et l’affichage,
* corriger quelques bugs ou améliorations demandées (nouvelle règle métier simple, nouveau calcul, etc.).

**Objectif pédagogique N2**
Apprendre à **améliorer et factoriser** un code PHP existant sans tout réécrire, et préparer la logique de “controller / modèle” qu’ils retrouveront dans Laravel.

### MVP — Transposer

**Description**
Les apprenants conçoivent un **mini-squelette d’appli PHP procédurale ou POO** (sans framework) pour un besoin simple (ex. gestion d’une petite liste d’articles ou de produits), qu’ils **pourront ensuite migrer vers Laravel**.

**Objectif pédagogique MVP**
Comprendre comment **organiser un petit projet PHP réel** (dossiers, fichiers, logique métier) et en faire un tremplin vers le back-end du fil rouge.

---

## ✅ Version 2 — Découverte Android Studio & Kotlin (maquette mobile)

### N1 — Imiter

**Description**
Les apprenants suivent un tuto pour :

* installer **Android Studio**,
* créer un projet Kotlin / Compose,
* faire un écran **liste d’articles simulés**,
* faire un écran **détail** avec navigation simple.

Les données sont dans une **liste Kotlin** en dur.

**Objectif pédagogique N1**
Découvrir l’**environnement Android** et la **syntaxe de base Kotlin/Compose**, et voir concrètement une **liste + détail** côté mobile avec des données simulées.

### N2 — Adapter

**Description**
À partir de cette maquette :

* changer la **structure des données** (ajout de champs, ex. catégorie, image),
* adapter la **UI** (carte, espacement, typographie),
* ajouter une **interaction** de base (clic sur un bouton, tri simple de la liste).

**Objectif pédagogique N2**
Savoir **adapter une maquette mobile existante** : modifier le modèle, la composable de liste, la composable de détail, sans repartir de zéro.

### MVP — Transposer

**Description**
Les apprenants créent une **nouvelle mini-app Compose** pour un autre type de contenu (ex. catalogue de formations, liste d’événements), avec :

* leurs propres modèles Kotlin,
* au moins 2 écrans (liste + détail),
* une navigation propre (arguments, gestion retour).

**Objectif pédagogique MVP**
Être capable de **concevoir une petite app mobile** autonome mais structurée, en réutilisant les patterns vus (liste/détail, composables, navigation).

---

## ✅ Version 3 — Interface publique minimale (sans base de données)

### N1 — Imiter

**Description**
Dans Laravel, les apprenants créent avec un tuto :

* une route pour la **liste d’articles**,
* une route pour la **page détail**,
* un contrôleur avec un **tableau PHP d’articles**,
* deux vues Blade simples pour afficher la liste et le détail.

Tout passe par le chemin **Route → Contrôleur → Vue** avec des données simulées.

**Objectif pédagogique N1**
Comprendre concrètement le **MVC Laravel** et le passage **données → contrôleur → vue** sur un cas ultra simple (liste + détail).

### N2 — Adapter

**Description**
À partir de cette interface publique minimale, les apprenants doivent :

* **adapter la structure** des données (ajout d’un champ, d’un tag…),
* modifier la vue pour **changer la présentation** (ordre, format de date, ajout d’un badge “Nouveau”),
* éventuellement **ajouter un second type de contenu** simulé (ex. “annonces” en plus des “articles”).

**Objectif pédagogique N2**
Apprendre à **faire évoluer une interface publique** en modifiant à la fois les données simulées, le contrôleur et les vues, sans casser le flux global.

### MVP — Transposer

**Description**
Les apprenants conçoivent une **variante de partie publique** pour un autre contexte (ex. “actualités d’un club”, “fiche formations”), en réutilisant la même logique Route → Contrôleur → Vue mais avec leurs propres choix d’informations et de design minimal.

**Objectif pédagogique MVP**
Être capable de **réutiliser la structure MVC de base** pour un **nouveau mini-projet de lecture de contenus**, en gardant un code lisible et cohérent.

---

## ✅ Version 4 — Base de données et modèle Article

### N1 — Imiter

**Description**
Les apprenants :

* configurent la **connexion MySQL** dans Laravel,
* créent les **migrations** pour `articles`, `categories`, `users` simples,
* créent le modèle `Article` + relations de base,
* insèrent quelques articles via seeders ou Tinker,
* adaptent la partie publique pour lire les articles **depuis la base**.

**Objectif pédagogique N1**
Faire le lien entre **schéma BD → migrations → modèles Eloquent → affichage web**, et comprendre comment les données “réelles” arrivent dans la vue.

### N2 — Adapter

**Description**
À partir du schéma existant, les apprenants doivent :

* **faire évoluer** une migration (ajouter un champ, ex. `excerpt`, `image_url`),
* mettre à jour les modèles et les vues,
* écrire quelques **requêtes Eloquent** plus ciblées (ordre, filtres simples).

**Objectif pédagogique N2**
Apprendre à **faire évoluer une base existante** proprement (migrations d’évolution) et à **adapter le code** pour intégrer ces changements.

### MVP — Transposer

**Description**
Les apprenants conçoivent un **petit MCD/MLD dérivé** pour un autre module (ex. commentaires, “auteurs invités”), puis :

* créent les migrations et modèles associés,
* relient ce module à `Article` (relations),
* l’intègrent (même simplement) dans la partie publique ou admin.

**Objectif pédagogique MVP**
Être capable de **concevoir et intégrer une nouvelle entité** cohérente dans la base de données du fil rouge, en respectant l’architecture existante.

---

## ✅ Version 5 — Espace d’administration et CRUD Article

### N1 — Imiter

**Description**
Les apprenants mettent en place le **back-office Article** avec Laravel :

* routes `/admin/articles/...`,
* contrôleur resource,
* formulaires de **création / modification**,
* liste des articles,
* bouton de **suppression**.

Tout reste **simple** : pas de status complexes, pas d’AJAX.

**Objectif pédagogique N1**
Savoir construire un **CRUD complet Laravel** et manipuler les formulaires, la validation de base et les requêtes HTTP principales.

### N2 — Adapter

**Description**
À partir de ce CRUD :

* améliorer la **présentation** de la liste (colonnes supplémentaires, tri simple),
* ajouter un champ supplémentaire dans les formulaires (ex. “image”, “mot-clé”),
* introduire éventuellement une **action de masse** simple (ex. supprimer plusieurs articles).

**Objectif pédagogique N2**
Apprendre à **adapter un module admin existant** aux nouveaux besoins sans casser ce qui fonctionne, en comprenant bien les impacts sur contrôleurs, vues et validations.

### MVP — Transposer

**Description**
Les apprenants conçoivent et implémentent un **nouveau CRUD complet** pour une autre entité (ex. `Category` gérée en admin, ou `Page` statique), avec :

* formulaires propres,
* validations pertinentes,
* éventuellement un mini-workflow (ex. “visible / caché”).

**Objectif pédagogique MVP**
Être capable de **concevoir et livrer un module admin complet** dans le fil rouge, de la BD jusqu’aux vues, en autonomie guidée par un cahier des charges.

---

## ✅ Version 6 — Sécurité et accès à l’admin (version alignée N1/N2/N3)

### 🎯 Rôle global

* Donner aux apprenants les **bases Laravel de la sécurité** (authentification + autorisation) en N1.
* Utiliser N2 pour **poser une infrastructure technique minimale avec Spatie** (installation + rôles simples) en restant faisable en ≈ 40 min.
* Utiliser N3 pour construire une **version proche d’un blog professionnel** : rôles, permissions, règles d’accès documentées, et **compléter toute la migration**.

---

### 🔧 Stack principale

* **Back-end**

  * Authentification Laravel mise en place avec **Laravel UI** (scaffolding classique : formulaires login/register, vues Blade de base).
  * Middlewares d’authentification et d’accès à certaines zones protégées.
  * Utilisation des **Gates Laravel en N1** pour contrôler les actions (accès admin, création/suppression d’articles).
  * Petit **aperçu des Policies** en fin de N1, pour préparer la transition vers N2/N3.

* **Base de données**

  * Table `users` pour l’authentification de base.
  * Champ booléen `is_admin` utilisé en N1 pour distinguer **Admin** et **Auteur**.
  * Tables supplémentaires créées par Spatie pour les rôles et permissions à partir de N2.

* **Spatie Laravel Permission**

  * Installé et utilisé **à partir de N2** pour gérer les rôles et permissions de manière structurée.

* **Interface (Blade)**

  * Layouts public + admin.
  * Affichage conditionnel de certains menus et boutons selon :

    * le fait d’être connecté ou non,
    * le profil logique “Admin” vs “Auteur”.

* **Git**

  * Commits thématiques autour de la sécurité :
    `feat: laravel-ui-auth`, `feat: gates articles`, `feat: accès admin`, `feat: spatie installation`, etc.

---

### 🟢 N1 — Imiter

*(inchangé)*

> **Objectif :** découvrir et imiter les **bases de la sécurité Laravel** avec Laravel UI et les **Gates**,
> sur un scénario simple Admin / Auteur.

#### 🔐 Authentification (bases avec Laravel UI)

En N1, l’apprenant :

* installe et configure **Laravel UI** pour générer le scaffolding d’authentification (formulaires de connexion, d’inscription, liens de déconnexion) ;
* vérifie que l’authentification fonctionne (inscription, connexion, déconnexion) ;
* protège l’accès à une zone administrateur par le middleware d’authentification ;
* teste les scénarios de base :

  * utilisateur non connecté : tentative d’accès à la zone admin → redirection vers la page de connexion ;
  * utilisateur connecté (Admin ou Auteur) : accès autorisé à la zone admin ;
  * après déconnexion : la zone admin redevient inaccessible.

#### 👥 Profils N1 : Admin vs Auteur (avec `is_admin`)

Pour simplifier, on définit **deux profils** uniquement via un champ booléen :

* **Admin** : `is_admin = true`
* **Auteur** : `is_admin = false`

Des utilisateurs de test sont créés pour représenter clairement ces deux profils.

**Règle fonctionnelle N1 sur les articles :**

* **Auteur (is_admin = false)**

  * peut **ajouter** de nouveaux articles ;
  * peut **supprimer uniquement ses propres articles**.
* **Admin (is_admin = true)**

  * peut **supprimer n’importe quel article**, quel que soit l’auteur ;
  * **ne peut pas ajouter** de nouveaux articles (aucun bouton ou lien de création pour lui).

Cette règle simple permet de montrer, dès N1, que deux utilisateurs connectés n’ont pas les mêmes droits.

#### 🔑 Autorisation N1 : focus sur les **Gates**

En N1, l’outil principal pour l’autorisation est la **Gate Laravel** :

* définition de Gates pour :

  * l’accès à certaines fonctionnalités réservées (par exemple, une action d’administration) ;
  * les actions sur les articles (créer un article, supprimer un article) ;
* utilisation des Gates :

  * côté contrôleurs, pour vérifier qu’un utilisateur a le droit d’effectuer une action donnée ;
  * côté vues Blade, pour afficher ou non certains boutons ou liens selon les droits de l’utilisateur.

La logique des Gates s’appuie sur :

* le fait que l’utilisateur soit connecté,
* la valeur du champ `is_admin`,
* l’éventuel lien entre l’utilisateur et l’article (ex. auteur de l’article ou non).

Les apprenants voient concrètement que :

* une Gate peut représenter : “Cet utilisateur a-t-il le droit de faire X ?” ;
* la vue et le contrôleur utilisent la même logique d’autorisation (centralisée dans les Gates).

#### 🔎 Petit aperçu des Policies (en imitation)

En fin de N1, on montre rapidement qu’il est possible de **centraliser les règles par modèle** avec une **Policy** (par exemple pour les articles), sans entrer dans tous les détails :

* idée : “au lieu d’écrire la logique d’autorisation partout, on peut la mettre dans une Policy associée au modèle” ;
* l’objectif est uniquement d’**introduire le concept**, pas de le maîtriser en profondeur.

🧠 **Objectif pédagogique N1**

* Comprendre par imitation :

  * la différence entre **authentification** (grâce à Laravel UI) et **autorisation** (grâce aux Gates) ;
  * comment un simple champ `is_admin` permet de distinguer un profil Admin et un profil Auteur ;
  * comment des **Gates** contrôlent des actions concrètes :

    * accès à la zone admin,
    * possibilité ou non d’ajouter / supprimer un article.
* Préparer le terrain pour N2 :

  * les apprenants ont déjà manipulé Gates et aperçu les Policies ;
  * ils sont prêts à remplacer la logique basée sur `is_admin` par un système plus riche de rôles et permissions.

---

### 🟡 N2 — Adapter

> **Objectif :** repartir du code N1 (fonctionnel avec Laravel UI + Gates) et **introduire Spatie de façon minimale**, avec un code réalisable en ≈ 40 min.
> N2 pose juste la **base technique des rôles**, toute la migration complète et les permissions avancées sont laissées à N3.

En N2, l’apprenant réalise un **petit bloc de travail concentré**, centré sur l’installation de Spatie et la création de deux rôles simples.

#### 🔐 Authentification

En N2 :

* l’apprenant **conserve telle quelle** l’authentification fournie par **Laravel UI** mise en place en N1 ;
* éventuellement, il ajoute **une redirection simple après connexion** (ex. Admin → `/admin`, Auteur → `/`), mais cette étape reste optionnelle et très limitée pour rester dans le temps imparti.

Aucune refonte d’UX ni de layout n’est exigée en N2 : ces améliorations sont repoussées à N3.

#### 🔑 Autorisation (introduction minimale de Spatie)

Le cœur de N2 est l’**intégration minimale** de Spatie Laravel Permission, réalisable en une courte séance :

1. **Installer et configurer Spatie Laravel Permission**

   * installer le package ;
   * publier la configuration ;
   * lancer les migrations Spatie ;
   * ajouter le trait nécessaire sur le modèle `User`.

2. **Créer les rôles de base**

   * créer deux rôles uniquement : **`admin`** et **`auteur`**,
     en cohérence avec les profils déjà utilisés en N1 ;

   * associer ces rôles aux utilisateurs de test existants (un Admin, un Auteur).

3. **Brancher un premier contrôle d’affichage / accès**

   * adapter **un seul endroit** (un menu, un lien ou une section) pour utiliser les rôles Spatie au lieu du simple `is_admin`, par exemple :

     * afficher un lien de menu seulement pour l’Admin,
     * ou afficher une section spécifique pour l’Auteur.

   * l’objectif est de montrer concrètement que :

     > “Le rôle Spatie change ce qui est visible / accessible dans l’interface.”

4. **Laisser le reste de la logique en mode N1**

   * les autres Gates, Policies et contrôles basés sur `is_admin` restent **tels quels** en N2 ;
   * la **migration progressive complète** (tous les contrôles `is_admin` → rôles/permissions Spatie, logique fine sur les articles, etc.) sera réalisée en **N3**.

🧠 **Objectif pédagogique N2**

* Montrer **comment intégrer une librairie réelle (Spatie)** dans un projet existant sans tout réécrire.
* Faire vivre aux apprenants un **petit “avant / après” concret** :

  * avant : contrôle basé sur `is_admin` ;
  * après : contrôle basé sur un **rôle Spatie**.
* Rester dans une charge de travail **codable en ≈ 40 min** :

  * installation Spatie,
  * création de 2 rôles,
  * assignation à 2 comptes,
  * un seul exemple d’utilisation dans l’interface.
* Préparer N3 :

  * les tables et rôles Spatie existent déjà ;
  * N3 pourra se concentrer sur :

    * compléter la migration,
    * ajouter de vraies permissions,
    * réfléchir aux règles métier.

---

### 🔴 MVP — Transposer (Version “Pro”)

*(texte global inchangé, mais il inclut maintenant implicitement la finalisation de la migration commencée en N2)*

> **Objectif :** s’appuyer sur Laravel + Spatie pour obtenir une **sécurité proche d’un blog professionnel**, claire et documentée.

En N3, le travail se focalise sur la **conception des règles métier** et la **complétion de la migration** :

* définition d’une **politique complète de rôles et permissions** (Admin, Auteur, Modérateur, etc.) ;
* utilisation de Spatie pour :

  * associer rôles et permissions aux utilisateurs ;
  * sécuriser finement les routes, les contrôleurs et les actions ;
* combinaison de Spatie et des **Policies Laravel** pour :

  * gérer proprement les droits sur les modèles (articles, commentaires…) ;
  * finaliser le remplacement des anciens contrôles `is_admin` par des rôles/permissions propres ;
  * garder une logique lisible et centralisée ;
* gestion claire des cas d’accès refusé (messages, redirections, cohérence entre ce qui est visible et ce qui est autorisé) ;
* production d’une **documentation synthétique** :

  * tableau “Rôle → Actions autorisées” ;
  * référence aux endroits où les règles sont implémentées (Gates, Policies, configuration Spatie, middlewares).

🧠 **Rôle du MVP**

* Proposer une version aboutie, utilisable comme **référence de projet fil rouge** pour la partie sécurité.
* Amener les apprenants à :

  * réfléchir aux règles d’accès comme à une vraie **conception métier** ;
  * faire le lien entre ce qu’ils ont imité en N1, adapté techniquement en N2, et ce qu’ils conçoivent en N3.

## ✅ Version 7 — API Articles

### N1 — Imiter

**Description**
Les apprenants créent l’API minimale :

* endpoint **liste** des articles publiés (`GET /api/articles`),
* endpoint **détail** d’un article (`GET /api/articles/{id}`),
* réponses **JSON** propres testées avec Postman.

**Objectif pédagogique N1**
Découvrir la logique **API REST simple** dans Laravel : routes API, contrôleurs, sérialisation en JSON, test de base avec un client externe.

### N2 — Adapter

**Description**
À partir de cette API :

* ajouter des **filtres** basiques (`?category=...`, `?search=...`),
* mettre en place une **pagination simple**,
* uniformiser les réponses JSON (toujours les mêmes clés, gestion minimale des erreurs).

**Objectif pédagogique N2**
Apprendre à **faire évoluer une API existante** pour la rendre plus utilisable, tout en gardant la compatibilité avec les clients.

### MVP — Transposer

**Description**
Les apprenants conçoivent un **petit cahier des charges API** (pour un module complémentaire : ex. commentaires, pages, catégories publiques) et :

* définissent les endpoints,
* les implémentent en respectant un style cohérent (codes HTTP, messages d’erreur, métadonnées simples).

**Objectif pédagogique MVP**
Être capable de **concevoir et exposer une API cohérente** pour un besoin précis du fil rouge, en pensant au client (web, mobile) qui va la consommer.

---

## ✅ Version 8 — Application mobile connectée à l’API

### N1 — Imiter

**Description**
Les apprenants :

* branchent l’app mobile sur l’API Laravel,
* remplacent les données simulées par des **appels HTTP** (`GET /api/articles`, `GET /api/articles/{id}`),
* affichent la liste et le détail à partir de la réponse JSON,
* gèrent un **message d’erreur simple** si l’API ne répond pas.

**Objectif pédagogique N1**
Comprendre le **dialogue back-end / mobile** : récupérer du JSON depuis Laravel et l’afficher correctement dans l’app Android.

### N2 — Adapter

**Description**
À partir de cette app connectée :

* améliorer la **gestion des états** (chargement, pas de données, erreur),
* utiliser des **paramètres de filtre / pagination** de l’API (si dispos en Version 6),
* adapter la UI pour rendre la liste plus lisible (groupement, tri, badges, etc.).

**Objectif pédagogique N2**
Apprendre à **adapter une app consommatrice d’API** quand l’API évolue, et à offrir une expérience utilisateur plus robuste (états réseau, cas sans données).

### MVP — Transposer

**Description**
Les apprenants conçoivent un **mini-projet mobile fil rouge** :

* sélectionnent un sous-ensemble d’API (articles, catégories, éventuellement autre module),
* structurent le code mobile (couche “data” séparée de l’UI),
* livrent une app plus complète (navigation, gestion d’erreurs, rafraîchissement, petit design cohérent).

**Objectif pédagogique MVP**
Être capable de **transposer toutes les notions web/API** dans une **vraie petite application mobile** cohérente, démontrable, alignée sur le projet fil rouge.

---

Si tu veux, je peux maintenant transformer une **version précise** (par ex. Version 4 CRUD) en **fichier README structuré** avec ces trois niveaux bien séparés pour ton dépôt.

