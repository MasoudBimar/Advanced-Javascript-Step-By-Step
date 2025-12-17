---
title: "Prototype"
lesson: true
index: 03
duration: 25m
prerequisites:
  - "Objects"
---

title: "Prototype"
lesson: true
index: 03
duration: 25m
prerequisites:

- "Objects"
  tags:
- prototype
- inheritance

---

# Prototype

Short summary: How prototypes work in JavaScript, prototype chains, and lookup semantics.

## Learning Objectives

- Explain the prototype chain and property lookup order.
- Use `Object.getPrototypeOf`, `__proto__`, and `Object.prototype` effectively.

## Example

```js
const a = { v: 1 };
const b = Object.create(a);
console.log(b.v); // 1 via prototype lookup
```

## Exercises

1. Inspect and modify an object's prototype at runtime and observe behavior.
