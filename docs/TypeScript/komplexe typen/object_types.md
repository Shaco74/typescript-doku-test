---
sidebar_position: 4
---

# Object Typen

Der Objekt Typ von TypeScript ist äußerst nützlich, da er uns eine extrem feine Kontrolle über Variablentypen in unseren Programmen ermöglichen. Sie sind auch die häufigsten benutzerdefinierten Typen.

```ts
let auto: {marke: string, bauJahr: string};
auto = {marke: "Audi", bauJahr: "2015"};

console.log(auto);
// -> { marke: 'Audi', bauJahr: '2015' }

console.log(auto.marke);
// -> Audi
```