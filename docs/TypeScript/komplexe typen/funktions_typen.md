---
sidebar_position: 6
---

# Funktion's Typen
JavaScript ermöglicht uns Funktionen Variablen zuzuweisen. Mit TypeScript können wir diese Variablen so typisieren, dass sie nur noch Funktionen annehmen nach unserem definierten Bedingungen.

```ts
type meinFunktionsTyp = (arg0: string, arg1: number) => string;
let meineVar: meinFunktionsTyp;

// Gültig
meineVar = function(p1: string, p2: number){
    return p1;
};

// Error: Der Typ "(p1: string, p2: string) => string" kann dem Typ "meinFunktionsTyp" nicht zugewiesen werden.
meineVar = function(p1: string, p2: string){
    return p1;
};

// Error: Der Typ "(p1: string, p2: number) => void" kann dem Typ "meinFunktionsTyp" nicht zugewiesen werden.
meineVar = function(p1: string, p2: number){
};
```