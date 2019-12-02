<h1> TP CSS </h1>

?> Vous pouvez l'inspecteur dans les outils développeur pour modifier du code CSS directement dans le navigateur.

?> Vous pouvez utiliser [des aides](https://developer.mozilla.org/fr/docs/Web/CSS/Reference) pour trouver les propriétés CSS.


## Exercices

Vous utiliserez le HTML suivant pour vos exercices : 
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Document</title>
</head>
<body>
  <header class="header">
    <nav class="nav">
      <div class="nav__item"><a class="nav__item__link" href="/">Home</a></div>
      <div class="nav__item"><a class="nav__item__link" href="/">About</a></div>
      <div class="nav__item"><a class="nav__item__link" href="/">Contact</a></div>
    </nav>
  </header>
  <main class="main">
    <article class="article">
      <header class="article_header">
        <h1 class="artile__header__title">Titre de l'article 1</h1>
      </header>
      <section class="artile__section">
        <img class="article__image" src="https://picsum.photos/300/200" alt="">
        <p class="article__description">lorem ipsum</p>
      </section>
    </article>
    <article class="article">
      <header class="article_header">
        <h1 class="artile__header__title">Titre de l'article 1</h1>
      </header>
      <section class="artile__section">
        <img class="article__image" src="https://picsum.photos/300/200" alt="">
        <p class="article__description">lorem ipsum</p>
      </section>
    </article>
    <article class="article">
      <header class="article_header">
        <h1 class="artile__header__title">Titre de l'article 1</h1>
      </header>
      <section class="artile__section">
        <img class="article__image" src="https://picsum.photos/300/200" alt="">
        <p class="article__description">lorem ipsum</p>
      </section>
    </article>
  </main>
</body>
</html>
```

### Exercice 1 : Inclure du CSS

1. Changer le style des liens (`<a>`) en mode inline.
2. Changer le style des liens (`<a>`) avec la balise `<style></style>` dans le `head`.
3. Changer le style des liens (`<a>`) en chargeant une feuille de style `<link rel="stylesheet" href="style.css">`.

Style: 
  - couleur du texte en gris | propriété: color
  - retirer le soulignement | propriété: text-decoration
  - au survol du lien afficher le soulignement | propriété: text-decoration

### Exercice 2 : Sélection basique

Dans une feuille de style sélectionner toutes les images et appliquer le style suivant:
  - une bordure noire de 1px
  - une bordure arrondi de 10px
  
### Exercice 3 : Sélection avancé

Dans une feuille de style sélectionner tout les articles qui sont frères adjacents `a + b` et appliquer le style suivant:
  - centrer les articles au milieu de l'écran
  - une bordure noire de 1px
  - ajouter une marge interne de 15px
  - ajouter une marge externe de 40px


Dans une feuille de style sélectionner tout les paragraphes `<p>` qui sont petits enfants de `<article>`, de parents inconnus `a * c` et appliquer le style suivant:
  - centrer le paragraphe au milieu du parent
  - ajouter un arrière-plan de couleur
  - au clique changer la couleur de l'arrière plan

### Exercice 4: Media queries

Dans une feuille de style: 
  - afficher le menu sur une seule ligne avec une marge de 16px à droite
  - lorsque la largeur de l'écran est inférieur à 640px, cacher la barre de navigation `display: none;`


### Exercice 5: Modèle de boite 

1. A l'aide float afficher les article sur 2 lignes avec une bordure de 1px noire et une marge entre les article de 40px
2. Refaire le même exercice avec des flexbox.



### Suite 

Si vous avez fini, vous pouvez faire les exercices de ce TP : [http://www.iut-fbleau.fr/sitebp/web/wim11/?p=tp3](http://www.iut-fbleau.fr/sitebp/web/wim11/?p=tp3)