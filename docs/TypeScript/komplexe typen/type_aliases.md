---
sidebar_position: 5
---

# Type Aliases

Anstelle immer wieder ein Objekt Typen zu neu deklarieren, kann man Typ Aliases nutzten. Sprich, man definiert sich einen Typ und gibt diesem eine(n) Variabel/Alias.
> Allgemein: type *alias name* = *type*

#### Beispiel:
```ts
// Vorher
let FirmaA: { 
  firmenName: string, 
  boss: { name: string, alter: number }, 
  angestellten: { name: string, alter: number }[], 
};

// Nachher
type Person = { name: string, alter: number };

let FirmaB: {
  firmenName: string, 
  boss: Person, 
  employees: Person[], 
};
```
