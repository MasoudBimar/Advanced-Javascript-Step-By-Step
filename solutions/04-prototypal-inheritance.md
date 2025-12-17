# Solutions — Prototypal Inheritance

## Exercise: convert constructor-based inheritance to composition

Constructor pattern (reminder):

```js
function Animal(name) { this.name = name; }
Animal.prototype.speak = function() { return `${this.name} makes a noise`; };

function Dog(name) { Animal.call(this, name); }
Dog.prototype = Object.create(Animal.prototype);
Dog.prototype.constructor = Dog;
```

Composition alternative:

```js
function createAnimal(name) {
  return {
    name,
    speak() { return `${name} makes a noise`; }
  };
}

function createDog(name) {
  const animal = createAnimal(name);
  return {
    ...animal,
    speak() { return animal.speak() + ' woof'; }
  };
}

const d = createDog('Rex');
console.log(d.speak());
```

Notes: Composition avoids shared prototype-state pitfalls and is easier to reason about and test.
