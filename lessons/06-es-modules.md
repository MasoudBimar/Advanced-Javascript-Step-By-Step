---
title: "ES Modules"
lesson: true
index: 06
duration: 25m
prerequisites:
  - "ES Classes"
tags:
  - modules
  - import
---

# ES Modules

Short summary: Module syntax, default vs named exports, dynamic import, and module resolution.

## Learning Objectives

- Use `export` / `import` in modern code and prefer named exports for clarity.
- Understand dynamic `import()` and top-level `await` (where supported).

## Example

```js
// utils.js
export function sum(a, b) { return a + b; }

// main.js
import { sum } from './utils.js';
console.log(sum(1,2));
```

## Exercises

1. Split a small module into two files and use both named and default exports.
