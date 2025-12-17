# Solutions — Prototype

## Exercise: inspect and modify prototype

```js
const base = { a: 1 };
const obj = Object.create(base);
console.log(obj.a); // 1 (from prototype)

// Modify prototype at runtime
Object.setPrototypeOf(base, { b: 2 });
console.log(obj.b); // 2

// Observations: lookup walks the prototype chain at access time.
```

Notes: Avoid frequently changing prototypes on hot objects — it's slow for engines.
