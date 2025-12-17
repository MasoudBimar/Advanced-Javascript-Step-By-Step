# Solutions — Objects

## Exercise: non-enumerable property

```js
const obj = { visible: 1 };
Object.defineProperty(obj, 'hidden', { value: 42, enumerable: false });

// Reading it:
console.log(obj.hidden); // 42

// It won't show in for..in or Object.keys
console.log(Object.keys(obj)); // ['visible']
console.log(Object.getOwnPropertyNames(obj)); // ['visible','hidden']
```

Notes: Use `Object.getOwnPropertyNames` or `Object.getOwnPropertyDescriptor` to inspect non-enumerable props.
