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

[![Le modulo en JavaScript](../images/JS-en-5-pts-01-09-concatenation-de-var.png)](https://www.youtube.com/watch?v=8GhaJBFO6Ws)

# JavaScript en cinq points
## 1.09 La concaténation de variables

La concaténation est le mot utilisé pour désigner le fait de rassembler deux chaînes de caractères pour en former une seule, ou comment coller les morceaux. On peut bien sûr assembler des chaines de caractère avec des 
variables. L'opérateur de concaténation est le signe plus (**+** ), et oui encore un piège de JavaScript, parce que le **+** additionne dans un contexte numérique et concatène dans les autres cas. 

Ci-dessous on assemble des chaînes de caractères avec des variables (auteur, personnage).

    var personnage = "Arsène Lupin ";
    var auteur = "Maurice Leblanc";
    console.log("Le personnage du roman de " + auteur + " se nomme " + personnage + 
    ".");

Dans ce cas c'est différent, on est dans un contexte numérique, + devient opérateur arithmétique de la somme, il ne concatène pas.

    var a = 2;
    var b = 8;
    console.log( a + b ); // 10

Observez bien les guillemets sur la valeur de la variable a.

    // cas 1 - chaîne de caractère + chiffre 
    var a = "2";
    var b = 8;
    console.log( a + b ); // 28

Ci-dessus la variable **a** contient une chaîne de caractère (string) à cause des guillemets . La variable b contient toujours un chiffre, donc le résultat n'est pas vingt-huit mais le caractère deux concaténé au chiffre huit. 

L'exemple suivant est le même en plus clair :

    // cas 2 - chaîne de caractère + chiffre (en plus clair)
    var a = "deux";
    var b = 8;
    console.log( a + b ); // deux8

Associons à présent une chaîne de caractère et des variables pour voir comment JavaScript interprète la concaténation. 

    // cas 3 - chaîne de caractère + chiffre + chiffre
    var a = "deux";
    var b = 8;
    var c = 5;
    console.log( a + b + c ); // deux85

.

    // cas 4 - chiffre + chiffre + chaîne de caractère
    var a = "deux";
    var b = 8;
    var c = 5;
    console.log( b + c + a ); // 13deux

Juste un conseil, ne mélangez pas les calculs avec les concaténations, c'est plus simple. :-D

*    MDN, Concaténation de chaînes : [ https://developer.mozilla.org/fr/docs/Learn/JavaScript/First_steps/Strings#Concat
%C3%A9nation_de_cha%C3%AEnes]( https://developer.mozilla.org/fr/docs/Learn/JavaScript/First_steps/Strings#Concat%C3%A9nation_de_cha%C3%AEnes)






