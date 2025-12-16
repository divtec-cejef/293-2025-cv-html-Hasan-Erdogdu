## A) Normalize.css doit être en local
- Le fichier `normalize.css` ne doit pas être chargé via un CDN
- Téléchargez-le et placez-le dans `css/normalize.css`
- Mettre à jour le lien dans le `<head>`

## B) Image dans un dossier `img/`
- L’image doit être placée dans un dossier `img/`
- Modifier les chemins :
  - `src="./img/Erdogdu_Hasan.JPG"`
  - `href="./img/Erdogdu_Hasan.JPG"`

## C) Sécurité du lien cliquable sur l’image
- Ajouter l’attribut :
  - `rel="noopener noreferrer"` sur la balise `<a>`

## D) Favicons : chemins relatifs
- Les favicons doivent être référencés avec `./`
- Exemple :
```
<link rel="icon" href="./favicon.ico">
```
- référencez les bonnes tailles d'icônes selon ce que vous écrivez dans le HTML (attribut `size`) --> utilisez le site favicon.io !

## E) Balise `<section>` mal fermée
- Une balise `<section>` n’est pas correctement fermée (ligne 60)
- Cela rend le HTML invalide
- Vérifiez bien l’ouverture et la fermeture de toutes les balises

## F) Texte alternatif de l’image
- L’attribut `alt` doit être plus descriptif
- Exemple :
  - `alt="Photo de Hasan D. Erdogdu"`

## G) paragraphes ou listes ?
- Si vous énumérez des choses, utiliser une liste. Mais si vous voulez "écrire"/"parler", utiliser un paragraphe.

 ## Autres
- Attention à l'indentation et à la lisibilité du code
