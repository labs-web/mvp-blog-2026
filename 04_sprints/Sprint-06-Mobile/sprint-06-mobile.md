# 📱 Sprint 6 : Application Mobile

## 📋 Pré-requis Pédagogiques
Pour réussir ce Sprint, vous devez avoir validé la session de formation suivante :

### 🎓 Sessions de Formation
*   ✅ **Session S8 :** Application Android (Interagir avec une API).
    *   *Acquis :* Création de l'application **"Ville Compagnon"** (Client News).

### 🔬 Labs & Veille
*   🧪 **Lab Retrofit :** Consommer une API REST en Java/Kotlin.
*   🧪 **Lab RecyclerView (ou LazyColumn) :** Afficher une liste performante.
*   📚 **Veille Material Design :** Composants natifs Android (Cards, AppBar).

## 1. 📝 Besoin
**Objectif :** Offrir une expérience de lecture native sur mobile Android en consommant l'API du Sprint 5.
*   L'application est une "Liseuse" : elle ne permet pas (encore) l'écriture.

## 2. 🔍 Analyse
*   **Cas d'Utilisation (Use Cases) :**
    *   **Voir le flux** : Liste verticale des derniers articles.
    *   **Lire** : Écran détail article.
    *   **Rafraîchir** : "Pull to refresh".
*   **Diagramme :** [sprint-06-mobile.puml](sprint-06-mobile.puml)

## 3. 🏗️ Conception
*   **Stack Mobile :**
    *   Langage : **Kotlin**.
    *   UI : **Jetpack Compose** (Recommandé) ou XML.
    *   Réseau : **Retrofit**.
    *   Images : **Coil** ou Glide.

## 4. 💻 Réalisation (Tâches Techniques)
### ⚙️ Contraintes Techniques Critiques
*   **Séparation des couches :** Modèle (Data Class) / Réseau (Interface API) / UI (Activity/Composable).
*   **Manifest :** Ne pas oublier la permission `android.permission.INTERNET`.

### Tâches Détaillées
*   **Android Studio :**
    *   [ ] Création projet "Empty Activity".
    *   [ ] Dépendances : Retrofit, Gson Converter, Coil.
    *   [ ] **Data Class :** `Article` (doit matcher le JSON du Sprint 5).
    *   [ ] **Service API :** Interface Retrofit `getArticles()`.
    *   [ ] **UI Liste :** Afficher Titre + Image miniature.
    *   [ ] **UI Détail :** Afficher l'article complet.

## Indice de solution
(Retrofit Service)

```kotlin
interface ApiService {
    @GET("api/articles")
    suspend fun getArticles(): Response<ArticleResponse>
}
```
