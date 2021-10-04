---
title: "Iterate over an array in JavaScript"

tags: [javascript]
categories: [software engineering]
---

## Using `for...of`

This is the simplest approach to iterate over an array while still allowing you to `break` out of the loop. 

Do not confuse with `for...in` which is for iterating over objects. 

```js
for (const element of array) {
    // your code here
}
```

## Using a `for` loop

This is the most versatile approach as it allows you to control the starting index, increment value, range, etc.

Use this approach if you're not doing a straightforward iteration over an array. For example, if you need to start at a different index or if you need to go through the array in reverse.

```js
for (let i = 0; i < array.length; i++) {
    // your code here
}
```

## Using `forEach`

The problem with this approach is that you may only skip to the next element with the `return` keyword, but you cannot `break` out of the loop.

As such, we generally avoid using this when we are writing solutions for interview questions because they may require us to exit early in order to optimize our solution. 

```js
array.forEach((item, index, array) => {
    // your code here
})
```
