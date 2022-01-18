---
sidebar_position: 7
---

# Generische Typen
In TypeScript können auch eigene generische Typen erstellt werden. Um einen eigenen generischen Typen zu initialisieren, nutzte das `type` keyword, gefolgt von eckigen Klammern `<..>`, in welche eine Variable als Platzhalter für den generischen Typen kommt.

 #### Beispiel:
 ```ts
type Mensch = {name: string, alter: number};
type Hund = {name: string, rasse: String};

type Familie<T> = {
    eltern: [T, T], kinder: T[]
};

let FamilieMensch: Familie<Mensch> ={
  eltern: [
    {name: "Mutter", alter: 45},
    {name: "Vater", alter: 50}
  ],
  kinder: [{name: "Kind", alter: 19}]
};

let FamilieHund: Familie<Hund> ={
  eltern: [
    {name: "Mutter", rasse: "Schäferhund"},
    {name: "Vater", rasse: "Rotweiler"}
  ],
  kinder: [
    {name: "Welpe1", rasse: "Schäferhund-Rotweiler-mix"},
    {name: "Welpe2", rasse: "Schäferhund-Rotweiler-mix"},
    {name: "Welpe3", rasse: "Schäferhund-Rotweiler-mix"},
    {name: "Welpe4", rasse: "Schäferhund-Rotweiler-mix"},
]};
]};
 ```