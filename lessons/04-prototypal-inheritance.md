---
title: "Prototypal Inheritance"
lesson: true
index: 04
duration: 30m
prerequisites:
  - "Prototype"
tags:
  - inheritance
  - prototype
---

# Prototypal Inheritance

Short summary: Patterns for inheritance in JS using prototypes and constructor functions.

## Learning Objectives

- Implement inheritance with constructor functions and `Object.create`.
- Understand pitfalls like shared mutable state on prototypes.

## Example

```js
function Animal(name) {
  this.name = name;
}
Animal.prototype.speak = function () {
  return `${this.name} makes a noise`;
};

function Dog(name) {
  Animal.call(this, name);
}
Dog.prototype = Object.create(Animal.prototype);
Dog.prototype.constructor = Dog;
```

## Exercises

1. Convert the constructor pattern to composition and discuss trade-offs.

## Exercises

1. Convert the constructor pattern to composition and discuss trade-offs.
