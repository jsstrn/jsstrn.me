---
title: "Set the lower and upper bound limits of a variable in JavaScript"
summary: "Use Math.min() and Math.max() to set the upper and lower bound limits of a variable"

tags: ["javascript"]
categories: ["software engineering"]
---

Here we want to create functions that allow us to count up and down a variable with a lower bound of 0.

We can achieve this easily with `Math.max()` which returns the higher of two values. So now if count falls below 0 it will default to 0 because `Math.max(-1, 0)` is 0.

```js
countDown = (count, min = 0) => Math.max(count - 1, min)

countDown(1) // => 0
countDown(-1) // => 0
```

Similarly, if you had to set the upper bound limit of a variable, you would use `Math.min()` because this would choose the smaller of the two numbers – `Math.min(101, 100)` is 100.

```js
countUp = (count, max = 100) => Math.min(count + 1, max)

countUp(99) // => 100
countUp(101) // => 100
```

## Reference

- [Math.min() – MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/min)
- [Math.max() – MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/max)
