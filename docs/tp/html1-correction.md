<h1> TP HTML 1 - CORECTION </h1>

### Exercice 1

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exercice 1</title>
</head>
<body>
  <h3>avec la balise ul/li</h3>
  <ul>
    <li><a href="https://facebook.com" target="_blank">https://facebook.com</a></li>
    <li><a href="https://google.com" target="_blank">https://google.com</a></li>
    <li><a href="https://amazon.com" target="_blank">https://amazon.com</a></li>
    <li><a href="https://microsoft.com" target="_blank">https://microsoft.com</a></li>
  </ul>
  <h3>avec la balise ol/li</h3>
  <ol>
    <li><a href="https://facebook.com" target="_blank">https://facebook.com</a></li>
    <li><a href="https://google.com" target="_blank">https://google.com</a></li>
    <li><a href="https://amazon.com" target="_blank">https://amazon.com</a></li>
    <li><a href="https://microsoft.com" target="_blank">https://microsoft.com</a></li>
  </ol>
  <h3>avec la balise dl/dt/dd</h3>
  <dl>
    <dt>HTML</dt>
    <dd>Hyper Text Markup Language</dd>
    <dt>CSS</dt>
    <dd>Cascade Style Sheet</dd>
  </dl>
  <h3>avec la balise table</h3>
  <table>
    <thead>
      <tr>
        <th>Site</th>
        <th>Lien</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>facebook</td>
        <td><a href="https://facebook.com" target="_blank">https://facebook.com</a></td>
      </tr>
      <tr>
        <td>google</td>
        <td><a href="https://google.com" target="_blank">https://google.com</a></td>
      </tr>
      <tr>        
        <td>amazon</td>
        <td><a href="https://amazon.com" target="_blank">https://amazon.com</a></td>
      </tr>
      <tr> 
        <td>microsoft</td>
        <td><a href="https://microsoft.com" target="_blank">https://microsoft.com</a></td>
      </tr>
    </tbody>
  </table>
</body>
</html>
```

### Exercice 2

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Excerice 2</title>
</head>
<body>
  <table>
    <thead>
      <tr>
        <th>Prénom</th>
        <th>Nom</th>
        <th>Photo</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Dennis</td>
        <td>Ritchie</td>
        <td><img src="./images/dennis.jpeg" alt="dennis ritchie" style="width:200px;"/></td>
      </tr>
      <tr>
        <td>Ada</td>
        <td>Lovelace</td>
        <td><img src="./images/ada.png" alt="Ada Lovelace" style="width:200px;"/></td>
      </tr>
      <tr>
        <td>Marie</td>
        <td>Curie</td>
        <td><img src="./images/marie-curie.png" alt="Marie Curie" style="width:200px;"/></td>
      </tr>
      <tr>
        <td>Linus</td>
        <td>Torvalds</td>
        <td><img src="./images/linus.jpeg" alt="Linus Torvalds" style="width:200px;"/></td>
      </tr>
    </tbody>
  </table>
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
