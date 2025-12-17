---
title: "Promises"
lesson: true
index: 07
duration: 35m
prerequisites:
  - "ES Modules"
tags:
  - async
  - promises
---

# Promises

Short summary: Promises, chaining, error handling, combinators, and `async`/`await`.

## Learning Objectives

- Create and consume `Promise` instances and use `.then`/`.catch` chains.
- Use `Promise.all`, `Promise.race`, and `async`/`await` idioms.

## Example

```js
function wait(ms) { return new Promise(res => setTimeout(res, ms)); }

async function raceExample() {
  const results = await Promise.all([wait(10).then(()=>'a'), wait(20).then(()=>'b')]);
  return results; // ['a','b']
}
```

## Exercises

1. Convert a callback-based API to return a Promise and demonstrate error handling.
