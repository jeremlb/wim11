<style>
img{display:block;margin:auto;}
table{ text-align: center;margin:0 auto;width: fit-content !important; }
</style>

<h1> TP HTML 2 </h1>

!> Vous validerez *toutes* vos pages avec le service de [validation](http://validator.w3.org/) du W3C.

?> Vous pouvez utiliser [des aides](https://websitesetup.org/wp-content/uploads/2019/10/WSU-HTML-Cheat-Sheet.pdf) pour trouver les balises HTML.

?> La correction se trouve là [correction](/tp/html2-correction)
 
## Exercices
### Exercice 1

Écrivez une page à partir du code suivant qui permet de reproduire l'image. Vous ne devez utilisez que des éléments `div` et `span`. 

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Exercice 1</title>
  <style>
    /* Ce code permet de mieux visualiser les éléments div et span. */
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

<body>>
</body>

</html>
```

![gallerie](/images/tp2-exercice-1.png ':-:')

### Exercice 2

Ecrivez une page tel que la capture d'écran suivante:
![gallerie](/images/tp2-exercice-2.png ':-:')

?>Il faut que le texte dans chaque partie soit long (au moins 2000 caractères), vous pouvez utiliser ce site pour générer du texte : [lorem ipsum](https://www.lipsum.com/)

Consigne : 
 - le premier lien doit vous emmener à l'ancre situé sur le titre `Ma première partie`
 - le second lien doit vous emmener à l'ancre situé sur le titre `Ma deuxième partie`
 - le troisème lien doit vous emmener à l'ancre situé sur le titre `Ma première partie` dans un autre fichier

?> Vous pouvez dupliquer le fichier que vous venez d'écrire dans le même dossier.

### Exercice 3

Écrivez une page contenant un formulaire qui demande à l'utilisateur de saisir son adresse e-mail et de choisir ses centres d'intérêt parmi sport, musique, lecture, cinéma et informatique. Ces derniers choix pourront être représentés par des cases à cocher ou une liste à sélection multiple.

Les informations recueillies seront envoyées par la méthode `GET` au script générique
```url
https://todo-wim.herokuapp.com/get
```

Le formulaire contiendra un bouton reset.

###### quelques conseils 
> Un formulaire est déclaré à l'aide de la balise `<form>`.
>
>  ```html
>    <form method="post" action="script" enctype="encodage" >....<form>
>  ```
>   1. l'attribut `method` précise le "mode d'envoie" des données : get ou post
>   2. l'attribut `action` précise l'url destinatrice des données
>   3. l'attribut `enctype` précise la façon d'encoder les données. Par défaut, `application/x-www-form-urlencoded`. Les autres valeurs possibles sont `multipart/form-data` et `text/plain`.
>
>  Les différents zones d'entrées (input) [ici](http://www.w3schools.com/html/html_form_input_types.asp).<br>
>  Utilisez l'attribut `name` pour donner un nom aux "variables" du formulaire transmises au serveur.<br>
>  Utilisez les **types html5** dédiés.<br>
>  Regardez aussi les attributs <b>placeholder</b>, <b>pattern</b>, et les balises `fieldset` et `label`.<br>
>

### Exercice 4

Écrivez une page contenant un formulaire qui demande diverses informations à l'aide de contrôles variés :


| Champ | Type |
| --- | --- |
| Nom | type text |
| Prénom | type text |
| Date de naissance | type date |
| Email | type email |
| Code postal | type number |
| Téléphone portable | type text |
| Sexe | boutons radio |
| Semestre | liste déroulante S1, S2, S3, S4. |
| Niveau en html | type range, entre 0 et 10 avec un pas de 1 |
| Message | zone de texte |


Tous les champs sont requis !<br>
Le formulaire contiendra un bouton reset, et submit.<br>
La requête résultante sera envoyée par la méthode `POST` au script générique
```url
https://todo-wim.herokuapp.com/post
```

### Exercice 5
Rajoutez (sans utiliser Javascript), les contrôles suivants au formulaire précédent :
- Le semestre S2 est sélectionné par défaut.
- Le code postal a 5 chiffres au maximum.
- Le niveau en html par défaut est 5.
- Le numéro de portable est un numéro français valide (10 chiffres commençant par 06 ou 07). En cas d'erreur, le navigateur affiche un message "Numéro à 10 chiffres sans espace et commençant par 06 ou 07".
