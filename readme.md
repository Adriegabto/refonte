#**Refont web : développement** 🚀 
![cover](./cover.PNG)
>Cette interface web à l’apparence très propre et bien designée, présente des erreurs de structuration. Les entêtes du document ne sont pas renseignées.
Par simple analyse écrite, minimum une page. Détaillez les points forts et faibles de cette page structurée en  HTML (_div vs semantique_) et css. Dans le validator W3C il y a 9 erreurs à corriger. Du coté css il faut appliquer l'unité de mesure REM :  n'oublié pas de déclarer la racine. Argumentez les erreurs que le développeur commet dans son approche techniques. Il y a également des erreurs d'accessiblité: veuillez m'en décrire quelques uns et m'expliquer la raison. A la fin de votre analyse réalisez la refonte de la page

> *Pour travailler plus confortablement procédez à un clône de ce dépôt git*.
> A la fin de votre réalisation créez un dépôt git avec l'affichage de la page d'index sur le navigateur.
> Trasmettez moi le lien sur mon spread-sheet que je vous est partagé. 
> L'exercice sera  noté /20

![AUR license](https://img.shields.io/aur/license/c)


**1ere erreur ligne 13**
Correction de la 1ere erreur a la ligne 13, nous pouvons voir qu'il manque le titre de la balise h2.
<h2 class="logo"></h2> -> Ajout d'un titre

**2eme erreur ligne 27**
Correction de la 2eme erreur, dans le "input" l'attribut "name" ne doit pas etre vide.
<input class="srch" type="search" name="" placeholder="Type To text"> -> Ajout d'une valeur dans l'attribu name

**3eme erreur ligne 28**
Correction de la 3eme erreur a la ligne 28, L'élément "a" ne doit pas apparaître comme descendant de l'élément "button". cette règle est imposé car les deux ont des utilisation differentes, le button est utilisé pour l'interaction avec l'utilisateur et la soummision de formulaire alors que les liens sont pour naviguer
<a href="#"> <button class="btn">Search</button></a>

**4eme erreur ligne 38**
Comme dans la précedente erreur, la balise "a" ne peut pas etre la descendante de "button"
<button class="cn"><a href="#">JOIN US</a></button> -> supression de la balise "a" pour un button "onclick" qui redigera vers la page choisi
-> <button onclick="window.location.href = '#'">JOIN US</button>

**5eme erreur ligne 43**
Comme vue auparavant, l'erreur est similaire a la 2eme, dans le "input" l'attribut "name" ne doit pas etre vide
<input type="password" name="" placeholder="Enter Password Here"> -> Ajout d'une valeur dans l'attribu name

**6 eme erreur ligne 44**
Comme vue dans l'erreur numero 3, l'element "a" de type lien de ne pas etre dans une boutton
<button class="btnn"><a href="#">Login</a></button>

**7 eme erreur ligne 47**
Correction de l'erreur, on peut voir que l'élement "a" qui possede un href englobe un autre élement </a> qui lui est fermant et en trop.
<a href="#">Sign up </a> here</a></p> -> <a href="#">Sign up here</a></p>

**8 erreur ligne 61**
Correction de l'erreur, div fermante en trop
</div> -> supression de la div

**9 eme erreur ligne 62**
Correction de l'erreur, div fermante en trop
</div> -> supression de la div