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

[![Le modulo en JavaScript](../images/JS-en-5-pts-02-04-00_ternaire.png)](https://www.youtube.com/watch?v=W9KlTvff32s)

# JavaScript en cinq points
## 2. Conditions
### 2.04.00 La condition ternaire

L'opérateur (ternaire) conditionnel est le seul opérateur JavaScript qui comporte trois opérandes. 

	/* l'instruction ternaire */	
		var age = 15;  
		var statut = age >= 18 ? "majeur" : "mineur";
		console.log(statut);

	/* l'équivalent avec l'instruction if else */
		var statut;
		var age = 15;  
		if ( age >= 18 ) {
			statut = "majeur";
		} else { 
			statut = "mineur";
		}
		console.log(statut);

Pour les ternaires à multiples instructions il faut utiliser l'instruction return, voir la doc sur MDN. 

MDN : Référence JavaScript > [L'opérateur (ternaire) conditionnel](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Operators/Conditional_Operator)

Créer un diagramme en ligne Draw.io : https://app.diagrams.net/