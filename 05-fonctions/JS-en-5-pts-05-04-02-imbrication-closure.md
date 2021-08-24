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

[![Le modulo en JavaScript](../images/JS-en-5-pts-05-04-02-imbrication-closure.png)](https://www.youtube.com/watch?v=1IPXLnt7ekg)

# JavaScript en cinq points

## 5. Fonction

### 5.04.02 imbrication

On peut imbriquer une fonction dans une fonction. La fonction imbriquée (interne) devient alors privée par rapport à la fonction (externe) qui la contient. Cela forme une fermeture (closure en anglais) qui ferme l'expression de la fonction c'est-à-dire que la fonction interne hérite des arguments et des variables de la fonction externe et donc contient la portée de cette dernière.

- Autrement dit, on ne peut accéder à la fonction interne qu' avec les instructions contenues dans la fonction externe.
- La fonction interne est une fermeture : la fonction interne peut utiliser les arguments et les variables de la fonction externe alors que le fonction externe ne peut pas utiliser de variable et d'arguments de la fonction interne.


        function externe( x ) {
            function interne( y ) {
                return x + y;
            }
            return interne;
        }
        var r1 = externe(3);     // undefined
        var r2 = interne(5);      // error
        var r3 = externe(3)(5); // undefined

ça marche pas hein ! Analysons :

- r1 : passe la valeur 3 en argument à X mais rien à Y.
- r2 : appelle la fonction privée interne() et on ne peut pas directement.
- r3 : On ne peut pas passer les argument X et Y via la fonction externe.


        function externe( x ) {
            var z = x;
            function interne( y ) {
                return  y + z;
            }
            return interne;
        }
        var r3 = externe(3)(5); // 8

Cette fois-ci ça marche, regardons pourquoi :

- On passe la valeur 3 à l'argument X de la fonction "externe", puis on stocke cette valeur dans la variable Z.
- L'appel de fonction passe une seconde valeur à l'argument Y de la fonction "interne". Rappelez vous que la fonction interne accède aux variables de la fonction "externe". Donc "interne" récupère bien la valeur de l'argument Y qui lui est adressé ainsi que la valeur de la variable Z qui stocke la valeur de l'argument X. La fonction "interne" retourne la somme de Y et Z qui est retourné par la fonction "externe".

En réalité l'exécution de la fonction "externe" est si rapide qu'on ne peut pas avoir le résultat de la fonction "interne", c'est pour cela qu'on l'appelle à la fin de la fonction "externe". L'appel se fait sans les parenthèses, rappelez vous que la fonction est une valeur et qu'elle a déjà reçu ses arguments (Z, Y).




#
Référence

MDN : Référence JavaScript > [Fonctions et portée des fonctions](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Functions)

[Quelle différence entre méthode et fonction ?](https://jacques-guizol.developpez.com/javascript/?page=page_5#LV-C)

MDN : Référence JavaScript > [L'objet Function](https://developer.mozilla.org/fr/docs/conflicting/Web/JavaScript/Guide#Lobjet_Function)

MDN : Référence JavaScript > [function](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Statements/function)

MDN : Référence JavaScript > [Fonctions](https://developer.mozilla.org/fr/docs/Web/JavaScript/Guide/Functions)