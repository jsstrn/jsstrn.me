---
title: What are truthy values in JavaScript?

tags: [javascript]
categories: [software engineering]
---

In JavaScript, [all values are truthy unless they are defined as falsy](https://developer.mozilla.org/en-US/docs/Glossary/Truthy). Here's a complete [list of falsy values](https://developer.mozilla.org/en-US/docs/Glossary/Falsy).

Any value that isn't falsy is by definition truthy. This means that an empty array `[]` or an empty object `{}` or a negative number are all considered truthy, but an empty string `""` is falsy.

Consider the following example,

```js
const name = "";

if (!name) {
  // your code here
}
```

While the code above works for checking for an empty string, the same cannot be said when checking for an empty array.

```js
const fruits = [];

if (!fruits) {
  // your code here
}
```

Here we are trying to check if `fruits` is an empty array. We cannot rely on type coercion in boolean context to check if `fruits` is an empty array.

```js
const fruits = [];

if (fruits.length === 0) {
  // your code here
}
```

This is also why we [should not use truthy matchers in test assertions](/notes/jest-avoid-tobetruthy-tobefalsy/).
