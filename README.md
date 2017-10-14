# rfc-js-destructuring-function-call
A proposal for JS syntax to destructure with a call to a function on an object.

```js
const {
  names(),
  other
} = myObject
```

equivalent to:

```js
const names = myObject.names()
const { other } = myObject
```

And possibly support nesting (with [rfc-js-declaration-identifier-from-leaf](https://github.com/AndersDJohnson/rfc-js-declaration-identifier-from-leaf)):

```js
const {
  nestedObject.names(),
  other
} = myObject
```

equivalent to:

```js
const names = myObject.nestedObject.names()
const { other } = myObject
```

Could be combined with [rfc-js-destructuring-creation](https://github.com/AndersDJohnson/rfc-js-destructuring-creation).
