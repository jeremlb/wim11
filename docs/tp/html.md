<h1> TP HTML </h1>

!> Vous validerez *toutes* vos pages avec le service de [validation](http://validator.w3.org/) du W3C.

?> Vous pouvez utiliser [des aides](https://websitesetup.org/wp-content/uploads/2019/10/WSU-HTML-Cheat-Sheet.pdf) pour trouver les balises HTML.

## Exercices
### Exercice 1

Écrivez une page contenant une liste de liens vers vos sites préférés (quatre ou cinq), avec le nom du site et une brève description de ce que l'on peut y trouver. Cette liste sera mise en forme à l'aide :
- D'une liste numéroté (balise ol)
- D'une liste non numéroté (balise ul)
- D'une liste de définition (balise dl)
- D'un tableau

Chaque lien devra s'ouvrir dans un autre onglet.

Configurez votre navigateur pour que l'affichage utilise l'encodage Unicode (UTF-8). Votre page ne doit pas être affectée. Si elle l'est, corrigez-la.

### Exercice 2

Ecrire une page qui affiche la gallerie de portraits suivante :

<style>img{display:block;margin:auto;}</style>
![gallerie](/images/gallerie.png ':-:')

?>Vous trouverez les images sur http://upload.wikimedia.org

### Exercice 3

Écrivez une page qui contient le tableau suivant, mais avec un "quart de tour", de sorte que les lignes deviennent les colonnes et vice-versa. Les coefficients devront être écrits en rouge.

<table>
  <thead>
    <tr>
      <th>Semestre</th>
      <th>Unité d'Enseignement</th>
      <th>Matière</th>
      <th>Coefficient</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="7" style="vertical-align:middle">S1</td>
      <td rowspan="3" style="vertical-align:middle">UE11</td>
      <td>AP</td>
      <td>6</td>
    </tr>
    <tr>
      <td>ASR</td>
      <td>5</td>
    </tr>
    <tr>
      <td>OMGL</td>
      <td>4</td>
    </tr>
    <tr>
      <td rowspan="4" style="vertical-align:middle">UE12</td>
      <td>ANG</td>
      <td>2,5</td>
    </tr>
    <tr>
      <td>EC</td>
      <td>2,5</td>
    </tr>
    <tr>
      <td>EGO</td>
      <td>5</td>
    </tr>
    <tr>
      <td>MATHS</td>
      <td>5</td>
    </tr>
  </tbody>
</table>

<!-- ### Exercice 4 -->

<!-- Ecrire une page qui envoie un formulaire à l'url : https://todo-wim.herokuapp.com/add-todo -->

<!-- Le formulaire doit contenir:  -->
 <!-- - un champ d'écriture avec le nom `todo` -->
 <!-- - un label -->
 <!-- - un bouton d'envoie  -->
 <!-- - un bouton reset -->

<!-- Une fois votre formulaire envoyé, vous serez redirigé sur la page : https://todo-wim.herokuapp.com. -->

## Aides

Vous trouverez quelques exemples d'utilisations de balises HTML.

### Structure d'un fichier HTML
```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Document</title>
</head>
<body>
  <h1>Hello World</h1>
</body>
</html>

```

### Les listes
[Plus de détails sur les listes](https://www.w3schools.com/html/html_lists.asp)
###### Liste à puces 
```html
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
```
<details>
  <summary>Exemple</summary>
  <ul>
    <li>Coffee</li>
    <li>Tea</li>
    <li>Milk</li>
  </ul>
</details>

###### Liste ordonnée
```html
<ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```
<details>
<summary>Exemple</summary>
  <ol>
    <li>Coffee</li>
    <li>Tea</li>
    <li>Milk</li>
  </ol>
</details>

### Les tables
[Plus de détails sur les tables](https://www.w3schools.com/html/html_tables.asp)
```html
<table>
  <tr>
    <th>Firstname</th>
    <th>Lastname</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Jill</td>
    <td>Smith</td>
    <td>50</td>
  </tr>
  <tr>
    <td>Eve</td>
    <td>Jackson</td>
    <td>94</td>
  </tr>
</table>
```
<details>
  <summary>Exemple</summary>
  <table>
    <tr>
      <th>Firstname</th>
      <th>Lastname</th>
      <th>Age</th>
    </tr>
    <tr>
      <td>Jill</td>
      <td>Smith</td>
      <td>50</td>
    </tr>
    <tr>
      <td>Eve</td>
      <td>Jackson</td>
      <td>94</td>
    </tr>
  </table>
</details>

<!-- ### Les formulaires -->
<!-- [Plus de détails sur les tables](https://www.w3schools.com/html/html_forms.asp) -->

<!-- Il existe plusieurs type de champs: -->
 <!-- - La balise input accepte plusieurs [types](https://www.w3schools.com/tags/att_input_type.asp)  -->
 <!-- - La balise [textarea](https://www.w3schools.com/tags/tag_textarea.asp) pour les zones de textes multilignes. -->

<!-- Il est aussi possible de [valider](https://developer.mozilla.org/fr/docs/Web/Guide/HTML/Formulaires/Validation_donnees_formulaire) des formulaires HTML sans utilisation de JavaScript. -->

<!-- ###### Balise form -->
<!-- ```html -->
<!-- <form action="URL" method="POST|GET"> -->
<!-- </form> -->
<!-- ``` -->

<!-- ###### Balise input -->
<!-- ```html -->
<!-- <input name="nom" id="nom" type="text"/> -->
<!-- ``` -->

<!-- ###### Boutons -->
<!-- ```html -->
<!-- <input type="submit" value="Envoyer"/> -->
<!-- <input type="reset" value="Reset"/> -->
<!-- ``` -->
