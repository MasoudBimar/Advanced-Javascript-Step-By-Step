---
title: "OOP Fundamentals"
---

title: "OOP Fundamentals"
lesson: true
index: 01
duration: 30m
prerequisites:

- "Basic JS syntax"
  tags:
- oop
- objects

---

# OOP Fundamentals

Short summary: Core object-oriented programming concepts and how they map to JavaScript.

## Learning Objectives

- Understand OOP principles: encapsulation, abstraction, composition, and polymorphism.
- Map these concepts to JavaScript patterns and language features.

## Prerequisites

- Basic JavaScript syntax and functions.

## Outline

1. OOP concepts overview
2. JS approaches: objects, prototypes, classes
3. When to use composition vs inheritance

## Example

```js
// Encapsulation via closures
function createCounter() {
  let count = 0;
  return {
    inc() {
      count++;
      return count;
    },
    get() {
      return count;
    },
  };
}

const c = createCounter();
c.inc(); // 1
```

## Exercises

1. Implement a small `Point` object with methods for distance and translation.

## Solutions

Provide solutions in `solutions/01-oop-fundamentals.md` or below when publishing.

## Author Checklist

- [ ] Metadata filled
- [ ] Example runnable
- [ ] Exercises present
