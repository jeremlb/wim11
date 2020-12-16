<h1> TP Js 1</h1>

<!-- ?> La correction se trouve là [correction](/tp/js1-correction) -->

?> Récupérer les fichiers sources utilisés pour le tp [ici](/tp/js-1-html-script)

## Exercices

Le TP est fait autour du jeu, le jeu de la vie. Les règles sont les suivantes : 
 - Une cellule morte possédant exactement trois voisines vivantes devient vivante. 
 - Une cellule vivante possédant deux ou trois voisines vivantes reste vivante, sinon elle meurt.

Une cellule est une unité de la grille. <br>
Pour faciliter les exercices la grille est carré. <br>
Un tour est appelé une génération.<br>


>Pour plus d'informations, voir la page [Wikipédia](https://fr.wikipedia.org/wiki/Jeu_de_la_vie)

> Le jeu est déjà coder, vous allez ajouter de nouvelle fonctionnalité au jeu dans ce TP.

### Exercice 1 : Inclure du JS

Charger le fichier `script.js` dans la page html `index.html`

> Il faut utiliser la balise `<script>` avec l'attribut `src` <br>
> Attention le tous les fichiers JavaScript doivent être chargée une fois que le DOM (la page HTML) est chargée. 

Vous devez avoir le résultat suivant : 

<style>img{display:block;margin:auto;}</style>
![gallerie](/images/js1-exercice-1.png ':-:')

### Exercice 2 : Ajouter un bouton reset

Ajouter un bouton nommée `reset` dans le HTML. Dans la fonction `main()` ajouter ce qui est nécessaire pour pourvoir remettre à zéro le jeu. <br>

> Pour remettre à zéro, il faut s'abonner à l'événement `click` sur le bouton reset, regarder comment le code est fait pour les autres boutons. <br>
> Il faut ensuite:
>  - stopper `autoplayInterval`, un timer est démarrer avec la fonctionnalité auto play
>  - détruire la grille courante avec la fonction `gridManager.destroyGrid();`
>  - créer un nouvel object `GridManager` avec `gridManager = new GridManager(gridSize, DIV_CONTAINER_ID)`
>  - initialiser le jeu avec `gridManager.setInitialState(INITIAL_STATE)`
><br><br>

> Vous avez des exemples dans le code


### Exercice 3 : Changer la taille de la grille

Vous allez ajouter un bouton qui permet d'afficher lors du clique une popin. Vous allez pouvoir renseigner la taille de la grille. 

> - Vous aurez besoin de la fonction [prompt](https://www.w3schools.com/jsref/met_win_prompt.asp)
> - La valeur que vous récupérer est un type `string` (équivalent à char[] en C), il faut donc parser le type string en integer avec la fonction [parseInt()](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Objets_globaux/parseInt)
> - Vous allez réutiliser la fonction reset que vous avez fait précédemment.

!> La grille est d'une taille minimum de 30.


### Exercice 4 : Afficher la taille de la grille dans l'interface

Vous allez afficher la taille à côté de la chaine de caractères `Taille de la grille:`. 

> - Utiliser `document.getElementById(GRID_SIZE_VAL_ID)` 
> - Utiliser la propriété `element.innerText = 'Hello World!`

### Exercice 5 : Afficher la génération courante

Vous allez afficher la taille à côté de la chaine de caractères `Génération numéro:`. 

> - Ajouter ce qu'il manque dans la fonction `computeNextGeneration(gridManager, generation)`
> - Penser à incrémenter la variable `génération`

### Exercice 6 : Vitesse d'execution du jeu

Vous allez créer un bouton : 
 - x1
 - x2
 - x10
 - x100

Lorsque le jeu est en mode auto play, il faut changer la vitesse à laquelle il faut appeler la fonction `computeNextGeneration(gridManager, generation)`. Si le jeu n'est pas en mode auto play mettre à jour la valeur de interval

> - Il faut pensez à stopper le `setInterval` et le démarrer avec la nouvelle vittesse de jeu
> - La vitesse normale du jeu est défini par la variable `GENERATION_INTERVAL`
> - x2 = `GENERATION_INTERVAL/2`, x10 = `GENERATION_INTERVAL/10`, etc.  

### Exercice 7 : (Bonus) Export de l'état de la grille

On veut pouvoir sauvegarder la partie pour la reprendre plus tard. Pour cela il faut enregistrer l'état du jeu. <br>
Créer une fonction d'export qui permet de : 
 - récupérer la taille de la grille, connaitre les coordonnées des cellules actives, la génération courante et la vittesse d'execution du jeu si mode auto play
 - sauvegarder l'état du jeu en `localStorage` lorsque l'on clique sur un bouton `Sauvegarder`


 > - Réutiliser la fonction `logCurrentGridState` qui permet d'afficher les coordonnées des cellules actives dans la console
 > - Un peu d'aide sur le [localStorage](https://developer.mozilla.org/fr/docs/Web/API/Window/localStorage)

### Exercice 8 : (Bonus) Reprendre une partie

A partir de l'exercice 7, écrire une fonction qui permet de reprendre une partie lorsque l'on clique sur un bouton `Reprendre` et si des données sont stockées en localStorage. 
