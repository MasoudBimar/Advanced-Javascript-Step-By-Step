---
title: "Collections"
lesson: true
index: 08
duration: 25m
prerequisites:
  - "Promises"
tags:
  - Map
  - Set
  - WeakMap
---

# Collections

Short summary: Built-in collection types in JS: `Map`, `Set`, `WeakMap`, `WeakSet`, and typed arrays.

## Learning Objectives

- Use `Map`/`Set` correctly and understand iteration order and common methods.
- Know when to use weak collections to avoid memory leaks.

## Example

```js
const m = new Map();
m.set({k:1}, 'value');
const s = new Set([1,2,3]);
```

## Exercises

1. Replace an object-as-map pattern with `Map` and explain differences.
