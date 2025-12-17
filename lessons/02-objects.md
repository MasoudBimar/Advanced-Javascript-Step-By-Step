---
title: "Objects"
lesson: true
index: 02
duration: 25m
prerequisites:
  - "OOP Fundamentals"
---

title: "Objects"
lesson: true
index: 02
duration: 25m
prerequisites:

- "OOP Fundamentals"
  tags:
- objects
- descriptors

---

# Objects

Short summary: Deep dive into JavaScript objects, property descriptors, and common object APIs.

## Learning Objectives

- Create and manipulate objects using literals, `Object.create`, and constructors.
- Understand property descriptors, freezing, sealing, and immutability patterns.

## Example

```js
const proto = {
  hello() {
    return "hi";
  },
};
const obj = Object.create(proto);
Object.defineProperty(obj, "x", { value: 42, writable: false });
```

## Exercises

1. Create an object with a non-enumerable property and show how to read it.
