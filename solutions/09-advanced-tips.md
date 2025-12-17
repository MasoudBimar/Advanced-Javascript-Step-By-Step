# Solutions — Advanced Tips

## Exercise: profile and low-cost optimization

Example function (inefficient):

```js
function sumSquares(arr) {
  // repeated property access and intermediate arrays
  return arr.map(x => x*x).reduce((s, v) => s + v, 0);
}
```

Low-cost optimization (single pass):

```js
function sumSquaresFast(arr) {
  let s = 0;
  for (let i = 0; i < arr.length; i++) {
    const v = arr[i];
    s += v * v;
  }
  return s;
}
```

When to optimize: profile first (DevTools, `console.time`) and only change hot code paths. Prefer readable code unless benchmarking proves otherwise.
