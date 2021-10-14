---
title: "Run JavaScript and TypeScript with RunJS"

tags: [javascript, typescript]
categories: [software engineering]
---

Often times I find myself wanting to run a bit of JavaScript code to check if it's working properly. I do this with my notes or when I'm trying to understand something I've read online.

Typically, I would use the console on my browser, but that has its limitations. There are also online tools like [JSFiddle](https://jsfiddle.net/), [CodePen](https://codepen.io/accounts/signup/user/free), and [Replit](https://replit.com/). However, these tools tend to be geared towards frontend development with HTML and CSS, and some even require you to login just to use their service.

I found a better solution is to use [RunJS](https://runjs.app/#platforms). It supports both JavaScript and TypeScript, has access to both Node.js and Web APIs, and generates live feedback as you type. Being a desktop application it's also a lot faster to access then an online tool.

RunJS works on Linux, Mac, and Windows. On macOS, install with Homebrew,

```js
brew install --cask runjs
```
