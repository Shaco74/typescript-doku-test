---
sidebar_position: 1
---

# Parameter

Um **Fehler Vorzubeugen**, indem Funktionen mit **falsche Datentypen** aufgerufen werden, können **Parameter in Funktionen auch Typen assigned** werden.

### Beispiel:

```ts
function print_length(word: string) {
  console.log(word + " ist " + word.length + " Zeichen lang.");
}
```

```ts
print_length("seb");
```

> gültiger Aufruf

```ts
print_length(232);
```

> Ungültiger Aufruf, wird in JavaScript nicht erkannt und wird als "undefined" behandelt, kann ich production zu einem fatalem error führen.

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
