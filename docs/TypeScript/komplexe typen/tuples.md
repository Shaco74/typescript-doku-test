---
sidebar_position: 2
---

# Tuples
Ein Array mit einer festen Größe ähnlicher oder unterschiedlicher Elementtypen, die in einer bestimmten Reihenfolge angeordnet sind, wird in TypeScript als Tupel definiert.
```ts
// Das ist ein Array
let array: string[] = ['Name', 'Alter', 'Vollzeit', 'Gehalt'];

// Das ist ein Tupel
let tuple: [string, number, boolean, number] = ['Jan', 22, true, 150000];
```

## .concat() auf einem Tuple
Wird .concat() auf einem Tupel aufgerufen wird ein Array zurückgegeben. (Da ein Tupel eine fixe Länge hat und nicht erweitert werden kann)
```ts
// Das ist ein Tupel
let tuple: [string, number] = ['Jan', 22];
let array = tuple.concat('Baesweiler', 'Deutschland');

console.log(array);
// In der Console wird ausgegeben: ['Jan', 22, 'Baesweiler', 'Deutschland']
```

## Spread Syntax
TypeScript's Tuple funktionieren einwandfrei mit dem JavaScript Spread Syntax, wenn die Parametertypen mit  den Elementtypen des Tuples übereinstimmen.
Mit dem Spread Syntax kann leicht ausgedrückt werden, dass jedes Element des Tuples als Parameter übergeben werden soll. Dabei ist es egal ob die Parameter der Funktion fix sind oder ob es sich um einen Rest Parameter des passenden Typen handelt
#### Beispiel:
```ts
let friends: [string, string, string] = ['Jan', 'Alice', 'Bob'];

//Beispiel Rest Parameter
function greetMyFriends1(...p: string[]): void{ 
    for(let person of p){
        console.log(person);
    }
 } 

 function greetMyFriends2(p1: string, p2: string, p3: string): void{ 
    console.log(p1);
    console.log(p2);
    console.log(p3);
}

//Aufruf von greetMyFriends mit allen Elementen von friends:
greetMyFriends1(...friends);
greetMyFriends2(...friends);
// Beide Aufrufe resultieren im selben Ergebnis

```