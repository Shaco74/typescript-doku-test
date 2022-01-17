---
sidebar_position: 3
---

# Enums

Enums in Typescript können auf drei Arten initialisiert werden. Wenn kein Wert den einzelnen Elementen zugewiesen wird, dann haben die einzelnen Elemente Werte inform von Indexen, sprich das erste Element hat den Wert 0 und das nächste ist jeweils inkrementiert um 1. Den Elementen können alternativ auch Werte zugewiesen werden, dies können **numbers** oder **strings** sein.

#### Beispiel:
```ts
enum Haustiere {
    Hund,       //Wert: 0
    Katze,      //Wert: 1
    Fische      //Wert: 2
}

console.log(Haustiere.Katze);
// -> 1

enum LagerBestand {
    Küchenmesser = 22, 
    Schneidebretter = 13,
    Silberbesteck = 43 
}

console.log(LagerBestand.Küchenmesser);
// -> 22

enum Richtung {
    Norden = "NORDEN", 
    Osten = "OSTEN", 
    Sueden = "SUEDEN",
    Westen = "WESTEN" 
}

console.log(Richtung.Norden);
// -> "NORDEN"
```

:::tip Tipp

Es ist Good Practice, wenn man einem **Enum einen String zuweist**, diesen in **Uppercase** zuschreiben. 

:::