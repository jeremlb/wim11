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
	<meta charset="utf-8">
  <title>Exercice 3</title>
  <style>
    table, th, tr, td {
      border: 1px solid black;
      text-align: center;
    }
  </style>
</head>
<body>
	<table style="border:1px solid black;">
		<tr>
			<th>Semestre</th>
			<td colspan=7>S1</td>
		</tr>
		<tr>
			<th>Unité d'Enseignement</th>
			<td colspan=3>UE11</td>
			<td colspan=4>UE12</td>
		</tr>
		<tr>
			<th>Matière</th>
			<td>AP</td>
			<td>ASR</td>
			<td>OMGL</td>
			<td>ANG</td>
			<td>EC</td>
			<td>EGO</td>
			<td>MATHS</td>
		</tr>
		<tr>
			<th>Coefficient</th>
			<td>6</td>
			<td>5</td>
			<td>4</td>
			<td>2,5</td>
			<td>2,5</td>
			<td>5</td>
			<td>5</td>
		</tr>
	</table>
</body>
</html>
```
