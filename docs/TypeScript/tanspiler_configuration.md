---
sidebar_position: 2
---

# Transpiler

> fehlt noch

## Configuration ( _tsconfig.json_ )

In der Config, kann festgelegt werden, wie **streng/strict** unsere TypeScript Code geschrieben werden muss, bis der Compiler meckert.

[Offizielle Typescript Dokumentation](https://www.typescriptlang.org/tsconfig)

### Beispielhafte config Datei:

```json
{
  "compilerOptions": {
    "target": "es2017",
    "module": "commonjs",
    "strictNullChecks": true
  },
  "include": ["**/*.ts"],
  "exclude": ["node_modules", "**/*.spec.ts"]
}
```

:::info info
Im Idealfall sollte die Config so strict wie möglich sein, dies resultiert möglicherweise dazu, dass der Code schwieriger zu schreiben ist, aber dafür einheitlicher und bugproofer ist.
:::
