---
date: 2021-01-05T01:21:42+08:00
title: "Beware the lame JavaScript interview question"

tags: ["interviews"]
categories: ["software engineering"]
---

This [question](https://www.interviewcake.com/question/javascript/js-scope?) is from [Interview Cake](https://www.interviewcake.com/).

```js
var text = 'outside'

function displayText() {
  console.log(text)
  var text = 'inside'
}

displayText()
```

What do you think will be output onto the console? 

It's not "outside". 

It's not "inside" either. 

It's actually "undefined" because of the hoisted variable.

The question is trying to test your understanding on variable hoisting when using the `var` keyword, but we should not even be using `var` in modern JavaScript in the first place. 

I would argue that this is not a good type of interview question. Being able to answer this question just tests how good of a compiler you are. Humans are not machines. It's far more important to determine what is bad code and to know how to retify it. 

The real issue with this code is that it is poorly written. All too often I see companies with interviews like these and then they wonder why their programmers write code so poorly. 

A better question might be to present the above code and ask the candidate if they see a problem with the code and then to refactor it so that there's no ambiguity. This would test the candidate's ability to identify bad code and to also refactor them.

The candidate might notice that the question uses `var` instead of `const` or `let` which may lead to unexpected behavior. Replacing `var` with `const` or `let` in this example, would yield an error – `Uncaught ReferenceError: can't access lexical declaration 'text' before initialization`.

The candidate can then write a test to assert the correct output and refactor the code to produce the desired outcome.
