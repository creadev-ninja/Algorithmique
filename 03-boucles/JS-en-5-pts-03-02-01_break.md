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

[![Le modulo en JavaScript](../images/JS-en-5-pts-03-02-01_break.png)](https://www.youtube.com/watch?v=CjqZG44UnuM)

# JavaScript en cinq points
## 3. Boucles
### 3.02.01 Interrompre une boucle *for* (break)

L'instruction break permet de terminer une boucle en cours d'instruction.

    for( compteur = 0; compteur < 10; compteur++ ) {
        if( compteur == 7 ){
            break;
        } else {
            console.log( compteur );
        }
    }    

SI la valeur de la variable compteur est égale à sept (7) on STOPPE la boucle. Autrement dit, si la condition est vrai on stoppe la boucle.

#
Référence

MDN : Référence JavaScript > [break](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Statements/break)