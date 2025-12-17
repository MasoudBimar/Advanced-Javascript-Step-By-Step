# Solutions — Collections

## Exercise: replace object-as-map with `Map`

Object-as-map (problematic when keys are objects):

```js
const mapLike = {};
mapLike[{}] = 'a'; // coerces key to "[object Object]"
```

Map solution:

```js
const m = new Map();
const key = { id: 1 };
m.set(key, 'value');
console.log(m.get(key)); // 'value'

// iteration
for (const [k,v] of m) console.log(k, v);
```

Notes: Use `WeakMap` for ephemeral keys tied to object lifetime to avoid memory leaks.
