<h1> TP HTML 2 - CORECTION </h1>

### Exercice 1

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Exercice 1</title>
  <style>
    div {
      border: 1px solid black;
      padding: 8px;
    }

    span {
      border: 1px solid red;
      padding: 4px;
    }
  </style>
</head>

<body>
  <div>
    ceci est une div qui prend l'espace d'un bloc
  </div>
  <div>
    ceci est une autre div qui prend l'espace d'un bloc
  </div>
  <div>
    ceci est encore une autre div qui prend l'espace d'un bloc. Mais cette fois-ci, il y a des éléments <span>de type
      inline</span> et je peux en mettre plusieurs sur une même ligne : <span>de type inline</span><span>de type
      inline</span><span>de type inline</span>
  </div>
</body>

</html>
```

### Exercice 2

#### premier fichier exercice-2.html
```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Exercice 2</title>
  <style>
  </style>
</head>

<body>
  <ul>
    <li><a href="#ancre-partie1">Partie 1</a></li>
    <li><a href="#ancre-partie2">Partie 2</a></li>
    <li><a href="./exercice-2bis.html#ancre-partie2">Partie 2</a></li>
  </ul>
  <h1>Mon article de blog</h1>
  <h2 id="ancre-partie1">Ma première partie</h2>
  <div>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Nisi voluptates corrupti atque culpa provident itaque
    debitis blanditiis. Architecto rem, quidem deserunt veritatis alias dolorem quasi cum asperiores. Reprehenderit
    harum, cum delectus qui nesciunt eos voluptas officia in, optio dolore consequatur officiis sed, impedit laboriosam
    magni nostrum alias tempore rerum temporibus earum expedita nulla! Voluptate, soluta accusamus.
  </div>
  <h2 id="ancre-partie2">Ma deuxième partie</h2>
  <div>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Nisi voluptates corrupti atque culpa provident itaque
    debitis blanditiis. Architecto rem, quidem deserunt veritatis alias dolorem quasi cum asperiores. Reprehenderit
    harum, cum delectus qui nesciunt eos voluptas officia in, optio dolore consequatur officiis sed, impedit laboriosam
    magni nostrum alias tempore rerum temporibus earum expedita nulla! Voluptate, soluta accusamus.
  </div>
</body>

</html>
```
#### premier fichier exercice-2bis.html
```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Exercice 2</title>
  <style>
  </style>
</head>

<body>
  <ul>
    <li><a href="#ancre-partie1">Partie 1</a></li>
    <li><a href="#ancre-partie2">Partie 2</a></li>
    <li><a href="./exercice-2bis.html#ancre-partie2">Partie 2</a></li>
  </ul>
  <h1>Mon article de blog</h1>
  <h2 id="ancre-partie1">Ma première partie</h2>
  <div>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Nisi voluptates corrupti atque culpa provident itaque
    debitis blanditiis. Architecto rem, quidem deserunt veritatis alias dolorem quasi cum asperiores. Reprehenderit
    harum, cum delectus qui nesciunt eos voluptas officia in, optio dolore consequatur officiis sed, impedit laboriosam
    magni nostrum alias tempore rerum temporibus earum expedita nulla! Voluptate, soluta accusamus.
  </div>
  <h2 id="ancre-partie2">Ma deuxième partie</h2>
  <div>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Nisi voluptates corrupti atque culpa provident itaque
    debitis blanditiis. Architecto rem, quidem deserunt veritatis alias dolorem quasi cum asperiores. Reprehenderit
    harum, cum delectus qui nesciunt eos voluptas officia in, optio dolore consequatur officiis sed, impedit laboriosam
    magni nostrum alias tempore rerum temporibus earum expedita nulla! Voluptate, soluta accusamus.
  </div>
</body>

</html>
```
### Exercice 3

```html
<!DOCTYPE html>
<html lang="fr">

<head>
  <meta charset="UTF-8">
  <title>Exercice 3</title>
</head>

<body>
  <form action="https://todo-wim.herokuapp.com/get" method="GET">
    <div>
      <label for="email">Email</label>
      <input id="email" type="email" name="email" required placeholder="Entrer un email">
    </div>
    <p></p>
    <div>
      <input type="checkbox" id="coding" name="interest" value="coding">
      <label for="coding">Développement</label>
    </div>
    <div>
      <input type="checkbox" id="music" name="interest" value="music">
      <label for="music">Musique</label>
    </div>
    <div>
      <input type="checkbox" id="art" name="interest" value="art">
      <label for="art">Art</label>
    </div>
    <div>
      <input type="checkbox" id="sports" name="interest" value="sports">
      <label for="sports">Sports</label>
    </div>
    <div>
      <input type="checkbox" id="cooking" name="interest" value="cooking">
      <label for="cooking">Cuisine</label>
    </div>


    <input type="reset" value="Réinitialiser">
    <input type="submit" value="Envoyer">
  </form>
</body>

</html>
```

### Exercice 4

```html
<!DOCTYPE html>
<html lang="fr">

<head>
  <title>Exercice 4</title>
  <meta charset="utf-8">
</head>

<body>
  <form method="POST" action="https://todo-wim.herokuapp.com/post">

    <div>
      <label for="lastname">Nom : </label>
      <input type="text" name="lastname" id="lastname" placeholder="ex: Dupont">
    </div>

    <div>
      <label for="firstname">Prénom : </label>
      <input type="text" name="firstname" id="firstname" placeholder="ex: Jean-Paul">
    </div>

    <div>
      <label for="birthdate">Date de naissance : </label>
      <input type="date" name="birthdate" id="birthdate">
    </div>

    <div>
      <label for="email">Adresse email : </label>
      <input type="email" name="email" id="email" placeholder="ex: jean-paul.dupont@gmail.com">
    </div>

    <div>
      <label for="postcode">Code postal : </label>
      <input type="number" name="postcode" id="postcode" placeholder="ex: 75000">
    </div>

    <div>
      <label for="phonenumber">N° Télephone portable : </label>
      <input type="text" name="phonenumber" id="phonenumber" placeholder="ex: 0655664488">
    </div>

    <div>
      <input type="radio" name="gender" id="femme" value="Madame">
      <label for="femme">Femme </label>
      <input type="radio" name="gender" id="homme" value="Monsieur">
      <label for="homme">Homme </label>
      <input type="radio" name="gender" id="autre" value="Autre">
      <label for="autre">Autre </label>
    </div>

    <div>
      <label for="semester">Semestre : </label>
      <select name="semester" id="semester">
        <option value="Semestre 1">Semestre 1</option>
        <option value="Semestre 2">Semestre 2</option>
        <option value="Semestre 3">Semestre 3</option>
        <option value="Semestre 4">Semestre 4</option>
      </select>
    </div>

    <div>
      <label for="niveau">Niveau en HTML (entre 0 et 10) : </label>
      <input type="range" name="niveau" id="niveau" min="0" max="10">
    </div>

    <div>
      <label for="message">Message : </label>
      <textarea name="message" id="message"></textarea>
    </div>

    <div>
      <input type="submit" value="Envoyer">
      <input type="reset" value="Remettre à zéro">
    </div>
  </form>
</body>

</html>
```

### Exercice 5

```html
<!DOCTYPE html>
<html lang="fr">

<head>
  <title>Exercice 5</title>
  <meta charset="utf-8">
</head>

<body>
  <form method="POST" action="https://todo-wim.herokuapp.com/post">

    <div>
      <label for="lastname">Nom : </label>
      <input type="text" name="lastname" id="lastname" placeholder="ex: Dupont">
    </div>

    <div>
      <label for="firstname">Prénom : </label>
      <input type="text" name="firstname" id="firstname" placeholder="ex: Jean-Paul">
    </div>

    <div>
      <label for="birthdate">Date de naissance : </label>
      <input type="date" name="birthdate" id="birthdate">
    </div>

    <div>
      <label for="email">Adresse email : </label>
      <input type="email" name="email" id="email" placeholder="ex: jean-paul.dupont@gmail.com">
    </div>

    <div>
      <label for="postcode">Code postal : </label>
      <input type="number" name="postcode" id="postcode" placeholder="ex: 75000" min="5" max="99999">
      <!-- 
          Validation d'un code postal avec une expression régulière
          <input type="text" name="postcode" id="postcode" placeholder="ex: 75000" pattern="(?:[0-8]\d|9[0-8])\d{3}">
         -->
    </div>

    <div>
      <label for="phonenumber">N° Télephone portable : </label>
      <input type="text" name="phonenumber" id="phonenumber" placeholder="ex: 0655664488" pattern="^(\+33|0)[6-7](\d\d){4}$">
      <!-- Il n'y a pas d'attribut pour afficher un message d'erreur personnalisé, c'est pour cela qu'il y a JavaScript -->
    </div>

    <div>
      <input type="radio" name="gender" id="femme" value="Madame">
      <label for="femme">Femme </label>
      <input type="radio" name="gender" id="homme" value="Monsieur">
      <label for="homme">Homme </label>
      <input type="radio" name="gender" id="autre" value="Autre">
      <label for="autre">Autre </label>
    </div>

    <div>
      <label for="semester">Semestre : </label>
      <select name="semester" id="semester">
        <option value="Semestre 1">Semestre 1</option>
        <option value="Semestre 2" selected>Semestre 2</option>
        <option value="Semestre 3">Semestre 3</option>
        <option value="Semestre 4">Semestre 4</option>
      </select>
    </div>

    <div>
      <label for="niveau">Niveau en HTML (entre 0 et 10) : </label>
      <input type="range" name="niveau" id="niveau" min="0" max="10" value="5">
    </div>

    <div>
      <label for="message">Message : </label>
      <textarea name="message" id="message"></textarea>
    </div>

    <div>
      <input type="submit" value="Envoyer">
      <input type="reset" value="Remettre à zéro">
    </div>
  </form>
</body>

</html>
```