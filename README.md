## TypeScript type System NO-OPs

Do you have a TypeScript project which is DOM-adjacent but doesn't use the DOM, such as a React Native project or something based on a Web Worker, Shared Worker, Service Worker or Audio Worker?

This npm module can be used with TypeScript 4.5's lib override features to create empty versions of lib files in TypeScript. A good case for this is for completely removing the DOM types if it becomes included via a transitive dependency:

```
{
  "dependencies": {
    "@typescript/lib-dom": "npm:@orta/type-noops"
  }
}
```

Would replace `dom` and `dom.iterable` with empty .d.ts files which don't affect the global types anywhere.