Fiche Web Design

JavaScript en 5 points
1.  Variables
2.  Conditions
3.  Boucles
4.  Tableaux
5.  Fonctions

[![CreaDev](../images/logo-creadev-210207-R-200.png)](http://www.creadev.ninja/)

Technologies en jeux : JavaScript

Vous avez juste besoin d’une navigateur et de sa console web.

[![Le modulo en JavaScript](../images/JS-en-5-pts-01-06-remontee-de-var.png)](https://www.youtube.com/watch?v=DdAypM6N_24)

# JavaScript en cinq points
## 1.06 Remontée de variable (*hoisting*)

Une chose étrange particulière à JavaScript est la possibilité, sans recevoir d'exception, de faire référence à une variable déclarée plus tard. Ce concept s'appelle remontée (*hoisting*) car les variables sont comme remontées en haut de l'instruction. 

Quand vous écrivez ceci 

    console.log(x);
    var x = 4;

c'est équivalent de cela

    var x;
    console.log(x);
    x = 4;

Dans les deux cas vous obtenez **undefined**

Si vous faites le test en console videz la entre les deux tests, sinon x est déjà déclaré, ou bien changer le nom de la variable en y par
exemple.

Parce que JavaScript remonte la déclaration de la variable, mais comme l'initialisation (l'affectation d'une valeur) est postérieure à l'appel du console.log, sa valeur est donc indéfinie. Le JavaScript n'est pas exécuté de la façon dont vous l'écrivez. 

#

*   MDN, Remontée de variables (hoisting) : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Guide/Types_et_grammaire#Remont%C3%A9e_de_variables_hoisting](https://developer.mozilla.org/fr/docs/Web/JavaScript/Guide/Types_et_grammaire#Remont%C3%A9e_de_variables_hoisting)


*   Grafikart : [https://www.grafikart.fr/tutoriels/scope-hoisting-770](https://www.grafikart.fr/tutoriels/scope-hoisting-770)
