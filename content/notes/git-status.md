---
title: "How to check the status of a Git repository"
summary: "Check the status of a Git repository"

tags: ["git"]
categories: ["software engineering"]
---

To check the status of the Git repository.

```bash
git status
```

We can see a `--short` or `-s` version with this command.

```bash
git status --short
```

For convenience, you can add `git st` as an alias.

```bash
git config --global alias.st "status --short"
```
