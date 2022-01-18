---
sidebar_position: 4
---

# Union mit literal Types

In TypeScript ist es auch möglich einen Typ mit einem Union zu beschreiben, welcher jedoch aus eigenen (Zustands-)Typen besteht. 
```ts
type Status = 'wartet' | 'arbeitet' | 'fertig';

function berichteStatus(status: Status): void{
    if(status === 'wartet'){
        console.log('Bereit für Anweisungen..');
    }
    else if(status === 'arbeitet')
    {
        console.log("In Arbeit!");
    }
    else if(status === 'fertig'){
        console.log("Anweisung ausgeführt!");
    }
}
```