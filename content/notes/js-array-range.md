---
title: "Create an array from range of numbers"
summary: "How to create an array of elements based on a range of numbers in JavaScript"

tags: ["javascript"]
categories: ["software engineering"]
---

Let's say we want to create a list of numbers from [0..9].

A simple approach would be to use a `for` loop

```js
const numbers = []

for (let i = 0; i < 10; i++) {
  numbers.push(i)
}

// numbers => [ 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 ]
```

Another approach is to use the `Array.prototype.keys()` method which returns the index of each element


```js
const numbers = [...Array(10).keys()]

// numbers => [ 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 ]
```

Perhaps the most elegant solution is to use `Array.from()`

```js
const numbers = Array.from({ length: 10 }, (_, i) => i)

// numbers => [ 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 ]
```

`Array.from()` takes an array-like object as its first argument and a map function that will be applied to each element. In this case, we pass an object with a `length` property and then we take just return the index from the map function.

If we wanted to start our list at 1 instead, then we can do this

```js
Array.from({ length: 10 }, (_, i) => i + 1)

// numbers => [ 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 ]
```

Or, more generally, if we wanted include 10 numbers starting from a certain number

```js
const startingNumber = 3

Array.from({length: 10}, (_, i) => i + startingNumber)

// numbers => [ 3, 4, 5, 6, 7, 8, 9, 10, 11, 12 ]
```

## References

- [Question in Stack Overflow](https://stackoverflow.com/questions/3895478/does-javascript-have-a-method-like-range-to-generate-a-range-within-the-supp#10050831)
- [Array.from() – 2ality](https://2ality.com/2014/05/es6-array-methods.html#array.from(arraylike%2C-mapfunc%3F%2C-thisarg%3F))
- [Array.from() – MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/from)
- [Array.prototype.keys() – MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/keys)
