---
sidebar_position: 2
---

# Type Guards

Um nun auch mit den Unions gescheit arbeiten zu können, nutzen wir sogenannte Type Guards. Dabei handelt es sich lediglich um if-Bedingungen die den Type einer Value prüfen, jedoch erweitert TypeScript diesen einzelnen if-Block um einige geschickte Funktionen. Nämlich, wird innerhalb eines Type Guards `returned` oder folgt ein `else` auf den TypeGuard ist der TypeScript Transpiler smart genug, um zu erkennen, dass es sich hinter dem TypeGuard um Code handeln muss, in welchem das Objekt den gegenteiligen Typen haben muss, als im Type Guard geprüft wurde. Dafür ein Beispiel:
:::caution Achtung
In einem Type Guard sollte man die geschweiften Klammern `{...}` ausschreiben, auch wenn es sich nur um ein einzeiliges return handelt.
:::
```ts
function numOrStr(p: string | number): void{

    // Type Guard der auf den Typen 'number' prüft
    if(typeof p === 'number'){
        console.log(p.toFixed(2));
    }
    // else-Block -> der transpiler erkennt an dieser stelle dass es sich nicht um eine 'number' handelt und es sich somit um einen 'string' handeln muss
    // Der Transpiler lässt nun string spezifische Methoden zu, da der Code an dieser Stelle auch logischerweise Typesafe ist.
    else{
        console.log(p.toLowerCase());
    }
}
```
:::info Info
Der TypeScript Transpiler gibt an die Entwicklungsumgebung auch das dementsprechende Feedback, bezüglich Type Guards. Im oberen Code-Beispiel wird die Variable `p` auch als string Type oder als number Type angezeigt, wenn man in einem Editor wie VS Code darüber hovert, abhängig davon ob man gerade im oberen Type Guard oder im else-Block ist.
:::

## Type Guard mit `in`
Will man nicht Prüfen ob das Objekt einem konkreten Objekt angehört, sondern ob eine gewisse Property besitzt, lässt sich das mit dem Schlüsselwort `in` verwirklichen. 
```ts
type Katze = {
  name: string;
  miauen: () => string;
}

type Maus = {
  name: string;
  piep: () => string;
}

function macheLaut(haustier: Maus | Katze) {

  if('miauen' in haustier){
    return haustier.miauen();
  }
  if('piep' in haustier){
    return haustier.piep();
  }
}
```