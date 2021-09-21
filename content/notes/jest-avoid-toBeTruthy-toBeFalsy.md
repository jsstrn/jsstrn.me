---
title: "Avoid using toBeTruthy() and toBeFalsy() matchers"

tags: ["jest", "software testing", "javascript"]
categories: ["software engineering"]
---

Test assertions should be explicit. 

If I'm trying to assert that something should be `true` I avoid using the [toBeTruthy()](https://jestjs.io/docs/expect#tobetruthy) matcher. 

It's important to realize that in JavaScript, [all values are truthy unless they are defined as falsy](https://developer.mozilla.org/en-US/docs/Glossary/Truthy). This means that as long as `result` is not a falsy value  (e.g. `false`, `""`, `null`, `undefined`, `NaN`, etc.), the assertion will pass. 

```js
expect(result).toBeTruthy() // passes if result is {} or [] or 1
```

Contrast it with this approach where `result` will only pass if its value is `true`.

```js
expect(result).toBe(true) // passes only if result is true
```

Similarly, if I am asserting that something should be `false` then I avoid using `toBeFalsy`.

```js
expect(result).toBeFalsy() // passes if result is "" or null or 0
```

In this case, the test case can only pass if its value is `false`.

```js
expect(result).toBe(false) // passes only if result is false
```
