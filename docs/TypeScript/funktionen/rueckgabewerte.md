---
sidebar_position: 2
---

# Rückgabewerte

### Typescript ist Smart

Genauso wie TypeScript einer Variabel einen Typen zuweist, indem es den Typ des zuzuweisenden Wertes erkennt.
Erkennt auch Typescript um welchen Typen von Rückgabewert es sich handelt.

### Beispiel:

```ts
function random() {
  return Math.random();
}
let num = random();
console.log(typeof num);
```

> num ist nicht any sondern bekommt den **Typen number** zugeschrieben, weil Typescript erkennt, dass in der return Zeile **Math.random()** eine number zurückgeben wird und somit **random()** insgesamt auch eine **number** zurück gibt.

### **Explizite** Typen der Rückgabewerte

man kann zwischen der schließenden runden Klammer und der öffnenden geschweiften Klammer einer Funktion einen **expliziten Typen des Rückgabewert definieren**

### Beispiel:

```ts
function random(): number {
  return Math.random();
}
```

> Dies ist nochmal sicherer und lesbarer als sich auf TypeScript zu verlassen den Rückgabewert zuerkennen.

```ts
function random(): void {
  console.log(Math.random());
}
```

> Genauso kann die Funktion auch als **void** deklariert werden
