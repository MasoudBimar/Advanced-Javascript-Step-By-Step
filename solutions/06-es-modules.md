# Solutions — ES Modules

## Exercise: split module into named and default exports

// utils/math.js

```js
export function sum(a, b) {
  return a + b;
}
export const PI = 3.14159;
export default function square(x) {
  return x * x;
}
```

// main.js

```js
import square, { sum, PI } from "./utils/math.js";
console.log(square(3));
console.log(sum(2, 2), PI);
```

Notes: Prefer named exports for reusable utilities; default exports are fine for a single primary export.
