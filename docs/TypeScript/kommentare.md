---
sidebar_position: 5
---

# Kommentare

Abseits von den standardmäßigen inline Kommentaren und Kommentarblöcken wie man sie aus JavaScript kennt, erweitert TypeScript unseren Code mit sogenannten **documentation comments**.

:::tip Tipp

**Documentation comments** helfen der Lesbarkeit und Nachvollziehbarkeit von Funktionen.

:::

#### Beispiel:

```ts
//  normales in-line Kommentar

/*
    normales
    multiline
    Kommentar
*/

/**
 * Returns the sum of two numbers.
 *
 * @param x - The first input number
 * @param y - The second input number
 * @returns The sum of `x` and `y`
 *
 */
function getSum(x: number, y: number): number {
  return x + y;
}
```

:::info info
in einem Editor wie VSCode wird nun diese selbstgeschriebene Dokumentation teilweise bis vollständig, als Tooltip angezeigt, je nachdem ob man über Komponenten wie ein Parameter mit der Maus hovert oder man über die Funktion hovert und die ganze Definition ausgegeben bekommt.
:::
