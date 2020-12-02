<h1> TP CSS 1 - CORECTION </h1>

### Exercice 1

#### exercice1.html

> Attention à la hiérarchie des déclarations : inline > style > fichier css
> Retirer `text-decoration: none;` de `<a style="color:grey;text-decoration: none;"` 
> pour que le soulignement au survol fonctionne

> Comme dit en cours préférer l'utilisation de class que de la sélection par balise HTML
> `nav__item__link` vs `a`

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Document</title>
  <link rel="stylesheet" href="exercice1.css">
  <style>
    .nav__item__link {
      color: grey;
      text-decoration: none;
    }

    .nav__item__link:hover {
      text-decoration: underline;
    }
  </style>

</head>

<body>
  <header class="header">
    <nav class="nav">
      <div class="nav__item"><a style="color:grey;text-decoration: none;" class="nav__item__link" href="/">Home</a>
      </div>
      <div class="nav__item"><a style="color:grey;text-decoration: none;" class="nav__item__link" href="/">About</a>
      </div>
      <div class="nav__item"><a style="color:grey;text-decoration: none;" class="nav__item__link" href="/">Contact</a>
      </div>
    </nav>
  </header>
  <main class="main">
    <article class="article">
      <header class="article_header">
        <h1 class="artile__header__title">Article title 1</h1>
      </header>
      <section class="artile__section">
        <img class="article__image" src="https://picsum.photos/300/200" alt="">
        <p class="article__description">lorem ipsum</p>
      </section>
    </article>
    <article class="article">
      <header class="article_header">
        <h1 class="artile__header__title">Article title 2</h1>
      </header>
      <section class="artile__section">
        <img class="article__image" src="https://picsum.photos/300/200" alt="">
        <p class="article__description">lorem ipsum</p>
      </section>
    </article>
    <article class="article">
      <header class="article_header">
        <h1 class="artile__header__title">Article title 3</h1>
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

#### exercice1.css
```css
.nav__item__link {
  color: grey;
  text-decoration: none;
}

.nav__item__link:hover {
  text-decoration: underline;
}
```


### Exercice 2

#### exercice2.css

> Comme dit en cours préférer l'utilisation de class que de la sélection par balise HTML
> `article__image` vs `a`

```css
.article__image {
  border: 1px solid black;
  padding: 4px;
  border-radius: 10px;
}
```

### Exercice 3

#### exercice3.css

```css
.article + .article {
  margin: 0 auto;
  border: 1px solid black;
  padding: 15px;
  margin:40px;
}

.article * .article__description {
  text-align: center;
  background-color: #FFFFDD;
}

.article * .article__description:active {
  background-color: indigo;
}
```

### Exercice 4

#### exercice4.css

```css
.nav .nav__item{
  display: inline-block;
}

.nav .nav__item:not(:last-child){
  margin-right: 16px;
}

@media (max-width: 640px) {
  .nav {
    display: none;
  }
}
```

>`visibility:hidden;` cache l'élément en gardant la place qu'il occupe dans la page, alors que `display: none;` cache l'élément et fait comme si il n'existait pas.

### Exercice 5

#### exercice5-float.css

```css
.article {
  width: calc(50% - 2 * 40px - 2 * 1px);
  margin: 40px;
  float: left;
  border: 1px solid black;
}
```

#### exercice5-flexblox.css

```css
.main {
  display: flex;
  flex-wrap: wrap;
}

.article {
  width: calc(50% - 2 * 40px - 2 * 1px);
  margin: 40px;
  border: 1px solid black;
}
```
