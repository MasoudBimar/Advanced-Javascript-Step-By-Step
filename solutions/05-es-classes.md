# Solutions — ES Classes

## Exercise: class hierarchy and static factory

```js
class Animal {
  constructor(name) { this.name = name; }
  speak() { return `${this.name} makes a noise`; }
}

class Dog extends Animal {
  speak() { return `${this.name} barks`; }
  static create(name) { return new Dog(name); }
}

const d = Dog.create('Buddy');
console.log(d.speak()); // Buddy barks
```

Notes: Use private fields (`#`) for internal state when you need true privacy; use static factories for alternate constructors.
