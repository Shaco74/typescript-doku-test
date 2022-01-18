---
sidebar_position: 1
---

# Was sind Unions

Wir haben bis hier hin gelernt, dass wir Typen nutzen können, um z.B. zu definieren, dass eine Funktionen nur mit einem Parameter von X Typen aufgerufen werden kann. Oder auch dass eine Variable nur Werte vom Typen Y annehmen darf. Andernfalls würden wir einfach einen **any Type** nutzen um auch mehr Typen zuzulassen. Was ist aber nun, wenn wir uns **nicht nur auf einen einzelnen Typen limitieren** wollen, noch uns auf einen losen **any Type** einlassen wollen?

Die Lösung sind Unions! Unions sind das Produkt von mehreren Typen. Ein Union wird ganz einfach über Typen und vertikale Striche `|` definiert, dabei agieren die Striche so wie ein **oder** in einer Bedingung.

#### Beispiel
```ts
// Variablen können per Union definiert werden
let artikelNummer: string | number;


// Genauso einfach werden auch Funktionsparameter als Union dargestellt 
function printArtikelNr(p: string | number){

}
```