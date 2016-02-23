# How to determine equality of two objects

_#javascript_ _#underscore_

As [AnthonyWJones points out](http://stackoverflow.com/a/201471/2040520):

> there is no generic means to determine that an object is equal to another

## Underscore.js

If you can use Underscore [the solution is rather simple](http://underscorejs.org/#isEqual):

```javascript
var stbn  = {name: 'Andrej', luckyNumbers: [1, 30, 1337]};
var clone = {name: 'Andrej', luckyNumbers: [1, 30, 1337]};
stbn == clone;          // false
_.isEqual(stbn, clone); // true
```
