---
sidebar_position: 3
---

# Variablen

Wenn eine Variabel **mit einem Wert initialisiert** wird, dann wird dieser Variabel der Type des Wertes zugeschrieben. Im gesamten **Scope** dieser Variabel kann, kann der Typ nicht überschrieben bzw. neu zugewiesen werden.

Alternativ, können Variablen mit Hilfe eines **Doppelpunktes** einen Typ zugewiesen bekommen.

Wird eine Variabel **ohne Wert initialisiert**, wird sie auch **nur dann als any Type zugelassen** und kann mit verschiedenen Datentypen beliebig oft beschrieben werden.

### Beispiel:

```ts
//  Variabel des Typen any
let anyType;

//  Beide Variablen sind vom Typ String, wobei der untere nur noch keinen Wert hat
let stringType = "Hello World";
let anotherStringType: string;
```

:::caution Achtung

Du solltest dich stets bemühen, jeder Variabel einen **festen Typen** zu geben.
Nutze also nur dann den **any Type**, wenn es notwendig ist.

:::
