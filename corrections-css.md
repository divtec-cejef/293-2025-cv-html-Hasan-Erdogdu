## A) Normalize.css chargé deux fois ❌

Actuellement :

* CDN
* fichier local

À corriger :

* **garder uniquement la version locale**

---

## B) Largeur maximale et centrage ❌

CSS actuel :
```
body {
max-width: 800px;
margin: 120px;
}
```

Problème :

* `margin: 120px;` **ne centre pas**
* ajoute un espace arbitraire sur tous les côtés

À corriger :
```
body {
max-width: 800px;
margin: 0 auto;
padding: 20px;
}
```

💡 *`margin: 0 auto` centre horizontalement un bloc.*

---

## C) Tailles de texte : unités incomplètes ⚠️

Actuellement :

* `em` utilisé (`h1 { font-size: 3em; }`) → ✅

Manque :

* une taille en `px`
* une taille en `rem`

Exemple possible :
```
h2 {
font-size: 24px;
}

p {
font-size: 1rem;
}
```

---

## D) Erreur de syntaxe CSS ❌

Dans `section` :
```
padding: 20px
border-radius: 8px;
```

❌ Point-virgule manquant

À corriger :
```
padding: 20px;
border-radius: 8px;
```
---

## E) Pseudo-classe hover incorrecte ❌

Actuellement :
```
a::hover {
color: #FF0033;
}
```

À corriger :
```
a:hover {
color: #FF0033;
}
```

---

## F) Images – règle globale trop contraignante ⚠️

CSS actuel :
```
img {
width: 180px;
height: auto;
}
```

Problème :

* toutes les images ont la **même largeur forcée**
* manque de flexibilité

À recommander :
```
img {
max-width: 100%;
height: auto;
}
```

Puis gérer les tailles avec des classes spécifiques.

💡 *Les règles globales doivent rester génériques.*

> *Le détail se gère avec des classes, pas avec des sélecteurs globaux.*

---

## Corrections HTML nécessaires (impact CSS)

### 1️⃣ Image cliquable : `href` incorrect ❌

Actuellement :
```
<a href="#./img/logo.png">
```

❌ `#` empêche l’ouverture du fichier

À corriger :
```
<a href="./img/logo.png" target="_blank">
```

💡 *Un lien vers un fichier ne doit jamais commencer par `#`.*

---
