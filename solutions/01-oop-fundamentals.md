# Solutions — OOP Fundamentals

## Exercise: `Point` object

Implementation (immutable-style factory):

```js
function createPoint(x = 0, y = 0) {
  return {
    x,
    y,
    translate(dx, dy) {
      return createPoint(this.x + dx, this.y + dy);
    },
    distanceTo(other) {
      const dx = this.x - other.x;
      const dy = this.y - other.y;
      return Math.hypot(dx, dy);
    },
  };
}

const p1 = createPoint(0, 0);
const p2 = p1.translate(3, 4);
console.log(p2.distanceTo(p1)); // 5
```

Notes: Factory preserves immutability, avoids `this` pitfalls, and is easy to test.
