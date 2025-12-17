---
title: "ES Classes"
lesson: true
index: 05
duration: 30m
prerequisites:
  - "Prototypal Inheritance"
tags:
  - classes
  - es6
---

# ES Classes

Short summary: Syntax and semantics of `class` in modern JavaScript, how it relates to prototypes.

## Learning Objectives

- Read and write ES `class` declarations and `extends` hierarchies.
- Understand `super`, static members, and private fields.

## Example

```js
class Animal {
  #secret = "x";
  constructor(name) {
    this.name = name;
  }
  speak() {
    return `${this.name}...`;
  }
}

class Dog extends Animal {
  speak() {
    return super.speak() + " woof";
  }
}
```

## Exercises

1. Implement a small class hierarchy and add a static factory method.
