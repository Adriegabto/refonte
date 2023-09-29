#**Refont web : développement** 🚀 
![cover](./cover.PNG)
>Cette interface web à l’apparence très propre et bien designée, présente des erreurs de structuration. Les entêtes du document ne sont pas renseignées.
Par simple analyse écrite, minimum une page. Détaillez les points forts et faibles de cette page structurée en  HTML (_div vs semantique_) et css. Dans le validator W3C il y a 9 erreurs à corriger. Du coté css il faut appliquer l'unité de mesure REM :  n'oublié pas de déclarer la racine. Argumentez les erreurs que le développeur commet dans son approche techniques. Il y a également des erreurs d'accessiblité: veuillez m'en décrire quelques uns et m'expliquer la raison. A la fin de votre analyse réalisez la refonte de la page

> *Pour travailler plus confortablement procédez à un clône de ce dépôt git*.
> A la fin de votre réalisation créez un dépôt git avec l'affichage de la page d'index sur le navigateur.
> Trasmettez moi le lien sur mon spread-sheet que je vous est partagé. 
> L'exercice sera  noté /20

![AUR license](https://img.shields.io/aur/license/c)


**Points fort et faible de page Structurée en div**

**Point fort div**

*flexibilité* : Les balises div sont géneriques, elles peuvent donc etre manipulées de maniere flexible pour une page personalisé et complexe

*Compatibilité* : Les balise "div" sont compatibles avec tous les navigateur

*Facilité* : Pour les développeurs moins familiers avec la semantique, les balises div sont plus simples

**Point faible div**

*Manque de sémantique* : le manque de sémantique peut nuire a l'accesibilité et au référencement

*Lourdeur* : L'utilisation excessive de balises <div> peut entraîner une structure HTML moins lisible et plus lourde

*Accessibilité* réduite : Sans balises sémantiques, les lecteurs d'écran et les moteurs de recherche peuvent avoir du mal à comprendre la structure et le sens du contenu.
 
**Point fort sémantique**

*Sémantique claire* : Les balises sémantiques comme <
header, nav, article, section, donnent une signification clair et ameliore le réferencement

*Meilleure compréhension* : Une structure sémantique rend le code HTML plus lisible et compréhensible pour les développeurs et les équipes de conception.

*Meilleure accessibilité* : Les lecteurs d'écran et les moteurs de recherche peuvent interpréter plus facilement le contenu, améliorant ainsi l'expérience utilisateur.

**Point faible sémantique**

*Complexité* : L'utilisation de balises sémantiques peut sembler plus complexe pour les débutants, car elles nécessitent une compréhension de la signification de chaque balise.

*Compatibilité* : Bien que la plupart des navigateurs modernes prennent en charge les balises sémantiques, certains anciens navigateurs peuvent avoir des problèmes de compatibilité.

*Moins de flexibilité* : Les balises sémantiques ont une signification préétablie, ce qui peut limiter la personnalisation et la créativité dans la mise en page.



****
**1ere erreur ligne 13**
Correction de la 1ere erreur a la ligne 13, nous pouvons voir qu'il manque le titre de la balise h2.
<h2 class="logo"></h2> => Ajout d'un titre

**2eme erreur ligne 27**
Correction de la 2eme erreur, dans le "input" l'attribut "name" ne doit pas etre vide.

```html
<input class="srch" type="search" name="" placeholder="Type To text">```
 -> Ajout d'une valeur dans l'attribu name


<input class="srch" type="search" name="recherche" placeholder="Type To text">
```

**3eme erreur ligne 28**
Correction de la 3eme erreur a la ligne 28, L'élément "a" ne doit pas apparaître comme descendant de l'élément "button". cette règle est imposé car les deux ont des utilisation differentes, le button est utilisé pour l'interaction avec l'utilisateur et la soummision de formulaire alors que les liens sont pour naviguer

```html
<a href="#"><button class="btn">Search</button></a> -> <a href="#">Search</a>
```

**4eme erreur ligne 38**
Comme dans la précedente erreur, la balise "a" ne peut pas etre la descendante de "button"
```html
<button class="cn"><a href="#">JOIN US</a></button>
``` 
-> supression de la balise "a" pour un button "aria-label" qui redigera vers la page choisi
```html
<button aria-label="link">JOIN US</button>
```

**5eme erreur ligne 43**
Comme vue auparavant, l'erreur est similaire a la 2eme, dans le "input" l'attribut "name" ne doit pas etre vide
```html
<input type="password" name="" placeholder="Enter Password Here"> 
```
-> Ajout d'une valeur dans l'attribu name
```html 
<input type="password" name="pwd" placeholder="Enter Password Here">
```

**6 eme erreur ligne 44**
Comme vue dans l'erreur numero 3, l'element "a" de type lien de ne pas etre dans une boutton
```html
<button class="btn"><a href="#">Login</a></button>
```

**7 eme erreur ligne 47**
Correction de l'erreur, on peut voir que l'élement "a" qui possede un href englobe un autre élement </a> qui lui est fermant et en trop.
```html
<a href="#">Sign up </a> here</a></p> -> <a href="#">Sign up here</a></p>
```

**8 erreur ligne 61**
Correction de l'erreur, div fermante en trop
</div> -> supression de la div

**9 eme erreur ligne 62**
Correction de l'erreur, div fermante en trop
</div> -> supression de la div



**Modification du HTML**

*Modifaction de la langue* en effet l'element "lang" est en anglais il est donc modifié pour etre en "fr"
```html
<html lang="fr">
```

*Ajout de meta dans le head*
```html
<meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Webpage Design & Development">
    ```

*Ajout h2* Ajout d'un titre dans la section h2

*Modifacation de la ligne 27* 
Rajout du "name" et ajout de la methode "sumbit" pour pouvoir soumettre la recherche
```html
<input class="srch" type="search" name="recherche" placeholder="Type To text">
```


**Modification des "px" en "rem"**