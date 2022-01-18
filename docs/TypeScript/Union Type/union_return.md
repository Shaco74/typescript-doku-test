---
sidebar_position: 3
---

# Union als return Type

Gibt eine Funktion mehr als einen Type potenziell zurück so wird auch der return Type Funktion als Union zusammengefasst.
```ts
function example(p: string | number){
    if(typeof p === 'string'){
        return p;
    }else{
        return p;
    }
}
// Der Typ des Rückgabewertes dieser Funktion wird als Union dargestellt: (string | number)

// let test: string | number
let test  =  example(2);

// Error: Der Typ "string | number" kann dem Typ "string" nicht zugewiesen werden.
let test2: string  =  example(2);
```