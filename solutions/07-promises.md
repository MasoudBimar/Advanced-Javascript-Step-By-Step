# Solutions — Promises

## Exercise: convert callback API to Promise

Callback-style function:

```js
function readFileCb(path, cb) {
  // fake async
  setTimeout(() => cb(null, `contents of ${path}`), 10);
}
```

Promisified version:

```js
function readFile(path) {
  return new Promise((resolve, reject) => {
    readFileCb(path, (err, data) => {
      if (err) reject(err);
      else resolve(data);
    });
  });
}

(async () => {
  try {
    const text = await readFile("/tmp/x");
    console.log(text);
  } catch (err) {
    console.error("error", err);
  }
})();
```

Notes: Always reject on errors and handle cleanup when necessary. For Node APIs prefer `fs.promises` or `util.promisify`.
