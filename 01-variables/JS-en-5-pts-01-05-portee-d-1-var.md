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

[![Le modulo en JavaScript](../images/JS-en-5-pts-01-05-portee-d-1-var.png)](https://www.youtube.com/watch?v=DdAypM6N_24)

# JavaScript en cinq points
## 1.05 La portée des variables

**Variable globale**

Lorsqu'une variable est déclarée avec **var** en dehors des fonctions, elle est appelée globale. Elle est disponible 
pour tout le code contenu dans le document. C'est pour cela qu'on déclare les variables au début du document. 

**Variable locale**

Lorsqu'une variable est déclarée avec var dans une fonction, elle est déclarée locale parce qu'elle est disponible 
qu'un sein de cette fonction. 

Testons ceci en déclarant le même nom de variable (mauvaise pratique) pour vérifier : 

        var maVariable = "soleil"; 
        function ciel() {
        var maVariable = "lune"; 
        console.log("depuis la fonction : " + maVariable); // locale
        }
        console.log("Depuis le document : " + maVariable); // globale

Que faut-il faire pour afficher le console.log qui se trouve dans la fonction ? Et bien lancer la fonction : 

        ciel(); 

**Différences entre var et let sur la portée de la variable.**

Si var est accessible depuis le document, let (depuis ES6) se limite au bloc de code auquel il appartient.

        if ( true ) {
        var x = 5;
        }
        console.log(x); // 5
        if ( true ) {
        let y = 5;
        }
        console.log(y); // undefined

Avec la version let, pour que la valeur soit retournée à console.log, il faudrait qu'il soit dans le bloc de code 
formé par le test if. On voit bien ici que **let** perd toute portée globale par rapport à **var**. 

Comparons la portée de var et de let :
#
déclaration de la variable avec let

    for(let i = 0; i<5; i++) {
    console.log("from loop : " + i);
    }
    console.log("from doc : " + i);

Le premier console.log affiche la valeur de i de 0 à 4.
Le second affiche un ReferenceError : i is not defined
car la variable i n'a pas été déclarée. 


Déclaration de la variable avec var

        for(var j = 0; j<5; j++) {
            console.log("from loop : " + j);
        }
            console.log("from doc : " + j);

ici la portée de la variable dépasse celle du bloc formé 
par l'instruction for et permet d'être récupéré dans le 
document. 
Si vous faites le test en console videz la entre les deux tests, sinon i est déjà déclaré, ou bien changer le nom de la variable en j par
exemple.
#
Et dans le cas particulier de la fonction : 

déclaration de la variable avec let

        function caddy() {
        console.log("from func " + elem);
        let elem = 'machin';
        }
        caddy();

Avec **Let** elem n'est pas remontée au début de la fonction donc pour console.log c'est comme si elle n'existait pas, d'où : *ReferenceError : can't acces lexical declaration 'elem' before initialization.*

 Déclaration de la variable avec var

        function caddy() {
        console.log("from func " + elem);
        var elem = 'machin';
        }
        caddy();

Avec **var** elem a été remontée sans affectation de valeur au début de la fonction. Elle reste donc indéfinie (undefined). C'est balot !

Si on faisait un console.log(elem) en dehors de la fonction, dans les deux cas elle serait **ReferenceError : elem is not defined**. Dans le cas de *let* parce que sa portée se rapporte à son bloc d'instruction, et dans le cas de *var* sa portée est locale à la fonction. 

Si vous faites le test en console videz la entre les deux tests, sinon elem est déjà déclaré, ou bien changer le nom de la variable en *lmt*
par exemple.

#
• 
MDN, Les portées de variables (scope) : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Guide/Types_et_grammaire#Les_port%C3%A9es_de_variables](https://developer.mozilla.org/fr/docs/Web/JavaScript/Guide/Types_et_grammaire#Les_port%C3%A9es_de_variables)





