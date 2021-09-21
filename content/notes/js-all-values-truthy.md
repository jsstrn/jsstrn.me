---
title: "What are truthy values in JavaScript?"

draft: true

tags: []
categories: []
---

In JavaScript, [all values are truthy unless they are defined as falsy](https://developer.mozilla.org/en-US/docs/Glossary/Truthy). Here's a complete [list of falsy values](https://developer.mozilla.org/en-US/docs/Glossary/Falsy). 

Any value that isn't falsy is by definition truthy. This means that an empty array `[]` or an empty object `{}` or a negative number are all considered truthy. 

For example, it's not uncommon to see code that looks like this

```js
const fruits = []

if (!fruits) {
  // your code here
}
```

You cannot rely on type coercion in boolean context to check if `fruits` is an empty array.

```js
const fruits = []

if (fruits.length === 0) {
  // your code here
}
```

This is also why we [should not use truthy matchers in test assertions](jest-avoid-toBeTruthy-toBeFalsy). 
