---
title: "Check if a variable is null or undefined in JavaScript"
summary: "Use double question mark operator to check if a variable is null or undefined in JavaScript"

tags: ["javascript"]
categories: ["software engineering"]
---

## Logical OR operator (||)

Let's say we want `value` to be set to `100` if `number` is `null` or `undefined`. 

```js
const number = null
const value = number || 100 // value => 100
```

While it seems this would work, we have a nasty bug in our code when `number` is initialized to `0`.

```js
const number = 0
const value = number || 100 // value => 100
```

The problem with using JavaScript's logical OR (`||`) operator is that `null`, `undefined`, `""`, and `0` all evaluate to false – they are [falsy](https://developer.mozilla.org/en-US/docs/Glossary/Falsy).

## Nullish coalescing operator (??)

A better appraoch is to use the double question marks.

The [nullish coalescing operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing_operator) is a logical operator that returns its right-hand side operand when its left-hand side operand is `null` or `undefined`.

```js
const number = 0
const value = number ?? 100 // value => 0
```

## Other approaches

We can use strict equality to check if a variable is `null` or `undefined` in JavaScript.

```js
if (number === null || number === undefined) {
  // value is either null or undefined
}
```

What I also found interesting is that although the regular equality in JavaScript is generally frowned upon, these two conditions are exactly identical. 

Of course, in general I would still prefer to use the code above as it is explicit in its intent.

```js
if (value == null) {
  // value is either null or undefined
}
```

Also, have a look at this [equality table](/notes/js-equality-table).
