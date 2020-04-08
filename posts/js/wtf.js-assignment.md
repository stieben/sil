# wtf.js: Assignment

_#javascript_ _#wtf_

Example 1:

```javascript
let x = 2;
console.log(7 * (x = 3)); // logs 21
```

Example 2:

```javascript
let a, b, c, d;
a = b = c = d = 5;
console.log(a + b + c + d); // logs 20
```

These work because assignments return the assigned value.
