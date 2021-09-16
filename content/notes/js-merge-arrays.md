---
title: "Merging arrays in JavaScript without duplicates"
summary: "How to merge two or more arrays in JavaScript"

tags: ["javascript"]
categories: ["software engineering"]
---

## TLDR;

⚠️ Note that this merge method will NOT work for an array of objects

```js
const a = [1, 2, 3]
const b = [3, 4, 5]

const c = [...(new Set([...a, ...b]))] // => [1, 2, 3, 4, 5]
```

Breakdown of steps

```js
// merge with duplicates
const m = [...a, ...b] // => [1, 2, 3, 3, 4, 5]

// remove duplicates with set
const s = new Set(m) // => Set [1, 2, 3, 4, 5]

// convert set to array
const c = [...s] // => [1, 2, 3, 4, 5]
```

## Explanation

Let's say we have these two arrays that we would like to merge together.

```js
const a = [1, 2, 3]
const b = [3, 4, 5]
```

One approach is to use `.concat`

```js
const c = a.concat(b) // => [1, 2, 3, 3, 4, 5]
```

Another approach is to use [destructuring](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment)

```js
const c = [...a, ...b] // => [1, 2, 3, 3, 4, 5]
```

In both cases, the problem is that there are duplicates in the merge. To ensure that there are no duplicates, we can use a [Set](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set). 

```js
const c = new Set([...a, ...b]) // => [1, 2, 3, 4, 5]
```

However, now `c` is a Set instead of an Array. 

```js
Array.isArray(c) // => false
```

To solve this, we can convert a Set into an Array with `Array.from`

```js
const c = Array.from(new Set([...a, ...b])) // => [1, 2, 3, 4, 5]
```

Another way is to simply use the spread operator

```js
const c = [...(new Set([...a, ...b]))] // => [1, 2, 3, 4, 5]
```
