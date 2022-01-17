---
sidebar_position: 1
---

# Parameter

Um **Fehler Vorzubeugen**, indem Funktionen mit **falsche Datentypen** aufgerufen werden, können **Parameter in Funktionen auch Typen assigned** werden.

#### Beispiel:

```ts
function print_length(word: string) {
  console.log(word + " ist " + word.length + " Zeichen lang.");
}

//gültiger Aufruf
print_length("Hallo");

//Ungültiger Aufruf, wird in JavaScript nicht erkannt. 
//Kann zu Error führen
print_length(232);
```


:::info Info
In TypeScript wird dieser Fehler schon vorher abgefangen und highlighted "argument is not assignable.." und compiled erst gar nicht.
:::

## Optionale Parameter

Parameter können auch in TypeScript optional sein, indem nach dem Parameter noch ein **Fragezeichen** gesetzt wird:

```ts
function greet(name?: string) {
  console.log(`Hallo, ${name || "User"}!`);
}
```

## Default Parameter

Parameter können auch in TypeScript optional sein, indem nach dem Parameter noch ein **Fragezeichen** gesetzt wird:

```ts
function greet(name = "User") {
  console.log(`Hallo, ${name}!`);
}
```

## Rest Parameter
Der Rest Parameter dient dem Zweck, beliebig viele Parameter einer Funktion zu übergeben. Dieser Rest Parameter kann einen Array eines expliziten Types haben oder auch ein Array vom Typ any sein.
```ts
// Rest Parameter vom Typ number (explizit)
function addAllTogether(...numbers: number[]): number{ 
    let result: number = 0;
    for(num of numbers)
      result += num;
    return result;
 }

// Rest Parameter vom Typ any
function printAll(...parameters): void{ ... }
```
