<h1> TP CSS 2 - CORECTION </h1>

> La correction utilise certaines techniques un peu avancé : 
> - variables css
> - pseudo élements
> - flexbox

```html
<!DOCTYPE html>
<html lang="fr">

<head>
  <meta charset="UTF-8" />
  <title>TP mise en page avec le css</title>
  <link rel='stylesheet' type='text/css' href='style.css'>
</head>

<body>
  <header class="header">
    <h2 class="header__title">Mon Panthéon</h2>
    <nav class="header__nav">
      <ul class="menu">
        <li class="menu__item"><a class="menu__item__link" href="#">Informaticiens</a></li>
        <li class="menu__item"><a class="menu__item__link" href="#">Mathématiciens</a></li>
        <li class="menu__item"><a class="menu__item__link" href="#">Sportifs</a></li>
        <li class="menu__item"><a class="menu__item__link" href="#">Musiciens</a></li>
      </ul>
    </nav>
  </header>
  <div class="main">
    <section class="main__content">
      <h2 class="main__content__title">Les informaticiens</h2>
      <div class="main__content__articles">
        <article class="article">
          <div class="article__description">
            <h3>Dennis <br>Ritchie</h3>
            <p><small>9 septembre 1941 - 12 octobre 2011</small></p>
            <p>Nationalité : américaine</p>
          </div>
          <img class="article__picture" alt="Ritchie"
            src="http://upload.wikimedia.org/wikipedia/commons/e/e6/Dennis_Ritchie.jpg">
        </article>
        <article class="article">
          <div class="article__description">
            <h3>Linus <br>Torvalds</h3>
            <p><small>28 décembre 1969 - </small></p>
            <p>Nationalité : finlandaise</p>
          </div>
          <img class="article__picture" alt="linus torvalds"
            src="http://upload.wikimedia.org/wikipedia/commons/7/71/Linus_Torvalds_cropped.jpeg">
        </article>
        <article class="article">
          <div class="article__description">
            <h3>Blaise <br>Pascal</h3>
            <p><small>19 juin 1623 - 19 août 1662</small></p>
            <p>Nationalité : française</p>
          </div>
          <img class="article__picture" alt="Pascal"
            src="http://upload.wikimedia.org/wikipedia/commons/7/79/Blaise_pascal.jpg">
        </article>
        <article class="article">
          <div class="article__description">
            <h3>Alan <br>Turing</h3>
            <p><small>23 juin 1912 - 7 juin 1954</small></p>
            <p>Nationalité : britannique</p>
          </div>
          <img class="article__picture" alt="turing"
            src="https://upload.wikimedia.org/wikipedia/commons/a/a1/Alan_Turing_Aged_16.jpg">
        </article>
      </div>
    </section>
    <aside class="main__aside">
      <p class="main__aside__description">
        <em><strong>Dennis MacAlistair Ritchie</strong></em>, né le 9 septembre 1941 à Bronxville dans
        l'État de New York et trouvé mort le 12 octobre 20111 à Berkeley Heights dans le New Jersey, est
        un des pionniers de l'informatique moderne, inventeur du langage C et
        codéveloppeur de Unix. Il est parfois désigné par dmr, son adresse électronique aux Laboratoires Bell.
      </p>

      <p class="main__aside__description">
        <em><strong>Linus Benedict Torvalds</strong></em>, né le 28 décembre 1969 à Helsinki en Finlande, est un
        informaticien
        américano-finlandais1. Il est connu pour avoir créé en 1991 le noyau Linux
        dont il continue à diriger le développement. Il en est considéré comme le « dictateur bienveillant ».
      </p>
      <p class="main__aside__description">
        <em><strong>Blaise Pascal</strong></em>, né le 19 juin 1623 à Clairmont (aujourd'hui Clermont-Ferrand) en
        Auvergne et mort le 19 août 1662 à Paris, est un mathématicien, physicien, inventeur, philosophe,
        moraliste et théologien français. Il invente, à 19 ans, la calculatrice mécanique.
      </p>

      <p class="main__aside__description">
        <em><strong>Alan Mathison Turing </strong></em>est un mathématicien, cryptologue et informaticien britannique.
        Il
        est l'auteur de l'article fondateur de la science informatique1 qui
        allait donner le coup d'envoi à la création des calculateurs universels programmables (ordinateurs). Il
        y présente sa machine de Turing et les concepts modernes de programmation et de programme.
      </p>
    </aside>
  </div>

  <footer class="footer">
    <a class="footer__link" href="mailto:mon-contact@u-pec.fr">Envoyer un mail</a>
    <a class="footer__link" href="#">Revenir à la page d'accueil</a>
  </footer>
</body>

</html>
```

```css
:root {
  --gray: #EFEFEF;
  --blue: #08c;
}

body {
  width: 960px;
  margin: 0 auto;
  font-family: Arial;
}

.header__title {
  padding: 16px;
  text-align: center;
  background-color: var(--gray);
}

.menu {
  text-align: center;
}

.menu__item {
  margin: 8px;
  position: relative;
  display: inline-block;
  list-style-type: none;
}

.menu__item::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  display: inline-block;
  border-top: 1px dashed var(--blue);
}

.menu__item__link {
  text-decoration: none;
  color: var(--blue);
}

.main {
  position: relative;
  display: flex;
  justify-content: space-between;
  width: 100%;
}

.main__aside {
  padding-left: 24px;
  border-left: 1px solid var(--gray);
  border-bottom: 1px solid var(--gray);
  text-align: justify;
}

.main__aside__description::before {
  content: '>>';
  color: var(--blue);
  margin-right: 8px;
}

.main__content {
  flex: 1 0 auto;
  width: 60%;
  display: flex;
  flex-direction: column;
  border-bottom: 1px solid var(--gray);
}

.main__content__title {
  text-align: center;
}

.main__content__articles {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
}

.article {
  min-width: 250px;
  width: 47%;
  margin-top: 8px;
  padding: 16px;
  display: flex;
  align-items: center;
  box-sizing: border-box;
  border: 1px solid var(--gray);
}

.article__description {
  width: inherit;
}

.article__picture {
  width: 100px;
  height: 100px;
  margin-left: 16px;
  ;
  padding: 2px 8px 16px 0;
  box-shadow: 10px 5px 5px #555;
}


.footer {
  display: flex;
  justify-content: space-between;
}

.footer__link {
  margin-top: 32px;
  color: var(--blue);
}
```
