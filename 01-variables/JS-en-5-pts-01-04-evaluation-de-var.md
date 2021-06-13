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

[![Le modulo en JavaScript](../images/JS-en-5-pts-01-04-evaluation-de-var.png)](https://www.youtube.com/watch?v=DdAypM6N_24)

# JavaScript en cinq points
## 1.04 L'évaluation des variables

MDN, Référence des erreurs JavaScript : https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Erreurs

Testez ce qui suit dans la console de votre navigateur :

1. **Une variable non déclaré** provoque une exception **ReferenceError** parce qu'on fait référence à une variable 
qui n'existe pas.

        console.log("La valeur de a est " + a); // ReferenceError

2. Une variable déclaré avant à l'aide de **var** mais sans valeur affectée donne par défaut undefined. Puisque sa valeur n'a pas été définie et donne donc la valeur par défaut : **undefined**.
 var a;

        console.log("La valeur de a est " + a); // undefined

3. Une variable déclaré après à l'aide de **var** mais sans valeur affectée donne par défaut *undefined*.

        console.log("La valeur de b est " + b); // undefined
        var b;

4. Une variable déclaré après à l'aide de **var** avec une valeur donne par défaut *undefined*. Il y a bien une remontée de la variable (voir plus bas chap. 6 hoisting) mais comme elle n'a pas été déclarée avant sa valeur 
reste indéfinie.
        
        console.log("La valeur de b est " + b); // undefined
        var b = 8;

5. Une variable déclarée avant à l'aide de **var** avec une valeur affectée plus loin donne *la valeur attendue*. Il y a bien une remontée de la variable possible puisque celle-ci a été déclarée au début même si elle a été initialisé 
plus loin.

        var b;
        console.log("La valeur de b est " + b); // 8
        b = 8;


6. Une variable déclarée après à l'aide de **let** mais sans valeur affectée donne **ReferenceError**. Il n'y a pas de remontée de la variable avec let comme on l'a vu avec var, c'est comme si la variable (lexicale) n'existait pas.

        console.log("La valeur de x est " + x); // ReferenceError
        let x;

7. Une variable déclarée avant à l'aide de let mais sans valeur affectée donne par défaut undefined.

       let y;
       console.log("La valeur de y est " + y); // undefined

8. Une variable déclarée avant à l'aide de **let** avec une valeur affectée donne la valeur attendue.

        let y = 45;
        console.log("La valeur de y est " + y); // 45

9. Une variable déclarée avant à l'aide de **let** avec une valeur affectée plus loin donne **undefined**. Contrairement
à var, avec let il n'y a pas de remontée de variable (voir plus haut le point 5).

        let z; 
        console.log("la valeur de z est " + z); // undefined
        z = 7;

10. On peut donc utiliser la valeur **undefined** pour déterminer si une variable possède une valeur. Ci-dessous le 
test sera valide puisque la variable n'a pas été initialisée mais seulement déclarée, sa valeur est donc indéfinie.

        var input;
        if(input === undefined) {
        console.log("oui");
        } else {
        console.log("non");
        }

11. La valeur **undefined** se comporte comme le booléen **false** lorsqu'elle est utilisée dans un contexte booléen. 
Ci-dessous on teste, avec l'instruction if, si le premier élément du tableau existe (monTableau[0]). Le tableau 
étant vide, il ne possède pas d'index 0 la réponse est donc **undefined**, l'équivalent de false en booléen

        var monTableau = new Array();
        console.log("La valeur de monTableau[0] : " + monTableau[0]);
        if(!monTableau[0]){
        console.log("Le tableau est vide."); // Le tableau est vide
        } else {
        console.log("Le tableau n'est pas vide");
        }


12. Essayons en ajoutant deux index au tableau. Donc monTableau[0] existe cette fois-ci, il ne peut donc pas 
être undefined puisqu'il y a une valeur associé à l'index 0.

        var monTableau = ["mangue", "coco"];
        console.log("La valeur de monTableau[0] : " + monTableau[0]);
        if(!monTableau[0]){
        console.log("Le tableau est vide.");
        } else {
        console.log("Le tableau n'est pas vide"); // Le tableau n'est pas vide
        }

13. Que se passe-t-il si on additionne un chiffre à une variable non initialisée ? ça devrait faire une sorte de 
undefined2, on concatène une valeur indéfinie avec un chiffre, dans le contexte numérique d'une addition, ce 
n'est donc pas un chiffre (**Not a Number**).

        var a;
        a + 2; // NaN

14. Une variable valant **null** est considéré comme 0 dans un contexte numérique. Et 0 fois 32 ça fait zéro.

        var n = null;
        console.log(n * 32); // 0
