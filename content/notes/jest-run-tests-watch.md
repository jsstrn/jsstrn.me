---
title: "Watch for file changes as you run your tests"
summary: "How to run your tests as your files change in Jest"

tags: ["jest", "software testing", "javascript"]
categories: ["software engineering"]
---

To watch for file changes and **only** run tests related to changed files. This requires that your project is a Git repository.

```bash
jest --watch
```

To watch for file changes and run **all** tests. This does not require that your project be a Git repository.

```bash
jest --watchAll
```

We often add this to our npm scripts

```json
{
  "scripts": {
    "test": "jest",
    "test:watch": "jest --watch"
  }
}
```

Reference: [Jest CLI documentation](https://jestjs.io/docs/en/cli.html#)
