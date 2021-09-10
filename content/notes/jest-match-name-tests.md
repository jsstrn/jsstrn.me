---
title: "Run Jest tests that match a describe block"
summary: "How to run tests that only match the name in the describe block"

tags: ["jest", "testing", "javascript"]
categories: ["software engineering"]
---

Very often I come across a situation where I'd like to only run a certain subset of tests in a describe block, usually when I'm trying to debug some code.

Let's say the describe block you want to run contains the word "Fizz Buzz"

```js
describe('Fizz Buzz', () => {
    // your tests here
})
```

You can run all describe blocks that match a regex pattern

```bash
jest --testNamePattern 'Fizz Buzz'
```

Or simply use the alias `-t` instead

```bash
jest -t 'Fizz Buzz'
```

Reference: [Jest CLI documentation](https://jestjs.io/docs/en/cli.html#)
