---
title: "Difference between for...of and for...in in JavaScript"

tags: [javascript]
categories: [software engineering]
---

## `for...of` is for arrays

The `for...of` statement iterates over values of an iterable (e.g. String, Array, Set, Map).

If we have 10 apples and we have 1 of them, we might say 1 of 10 apples. That's one way to remember that `for...of` is for arrays.

```js
const array = ['a', 'b', 'c']

for (const element of array) {
    // element => 'a', 'b', 'c'
}
```

## `for...in` is for objects

The `for...in` statement iterates over properties of an object, in an arbitrary order.

In JavaScript, arrays are also objects so you can use `for...in` on an array, but the results are probably not what you would expect.

The way I like to remember this is "`for...in` objects" sounds like "foreign objects".

```js
const object = { a: 1, b: 2, c: 3 }

for (const key in object) {
    // key => a, b, c
    // object[key] => 1, 2, 3
}
```