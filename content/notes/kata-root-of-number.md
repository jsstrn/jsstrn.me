---
title: "Find the root of a number"

tags: [kata]
categories: [software engineering]
---

## Question

Implement a function `root` that calculates the n'th root of a number.

The function takes a non-negative number `x` and a positive integer `n` and returns the positive n'th root of `x` within an error of 0.001.
Suppose the real root is `y`, then

```txt
|y - root(x, n)| < 0.001
```

## Solution

{{% collapse title="Reveal solution" %}}

```js
/*
time complexity: O(n)
space complexity: O(1) 
*/

function root(x, n) {
  if (n === 0) {
    return 0;
  }

  if (n === 1) {
    return x;
  }

  let lower = 0;
  let upper = x;
  let guess = (upper + lower) / 2;
  let tolerance = 0.001;

  let isWithinTolerance = () => Math.abs(Math.pow(guess, n) - x) < tolerance;

  while (!isWithinTolerance()) {
    let result = Math.pow(guess, n);

    if (result > x) {
      // guess is too high
      upper = guess;
    } else if (result < x) {
      // guess is too low
      lower = guess;
    } else {
      break;
    }

    guess = (upper + lower) / 2;
  }

  return guess;
}
```

{{% /collapse %}}
