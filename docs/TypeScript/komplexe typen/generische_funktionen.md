---
sidebar_position: 8
---

# Generische Funktionen
In TypeScript können auch Funktionen Parameter von generischen Typen erhalten und auch generische Typen zurückgeben. Der generische Typ wird hier nach dem  Funktionsnamen beschrieben `function <T> (p1: T){ ... }`

#### Beispiel
```ts
function printGenerisch <T> (p: T): void{
  console.log("Der wert: " + p + " und der Typ: " + typeof(p));
}

// -> Der wert: 1234 und der Typ: number
printGenerisch<number>(1234);
// -> Der wert: Hallo und der Typ: string
printGenerisch<string>("Hallo");
```