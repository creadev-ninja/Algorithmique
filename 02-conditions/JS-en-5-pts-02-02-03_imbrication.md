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

[![Le modulo en JavaScript](../images/JS-en-5-pts-02-02-03_imbrication.png)](https://www.youtube.com/watch?v=W9KlTvff32s)

# JavaScript en cinq points
## 2. Conditions
### 2.02.03 L'imbrication de if

On peut parfaitement imbriquer les conditions, mais attention à ne pas faire des complications inutiles.

    if ( condition-1 ) {  
		   /* le bloc de code est exécuté 
           si la condition est true (vrai) */

			if ( condition-2 ) {  
				   /* le bloc de code est exécuté 
                   si la condition-2 est true (vrai) */
			} else {
				   /* mais si la condition-2 est évalué à false (faux) 
                   c'est ce bloc de code qui s'exécute */
			}
	} else {
		   /* mais si la condition-1 est évalué à false (faux) 
           c'est ce bloc de code qui s'exécute */
	}

Exemple

    var heure = new Date().getHours(); 
	var salutation;

	if ( heure > 12 ) {
		if ( heure < 19 ) {
			salutation = "Bonne journée";
		} else {
			salutation = "Bonne soirée";
		}
	} else {
			salutation = "bonjour ";
	}
	console.log(salutation);


Observez le [diagramme](../images/diagram/diagram-if-3.png), il faut que les conditions soient vrai pour qu'elles s'enchaînent (à la différence du chapitre suivant). 