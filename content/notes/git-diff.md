---
title: "View code changes"
summary: "View code changes with <code>git diff</code>"

tags: ["git"]
categories: ["software engineering"]
---

One way to review code changes that are unstaged is to use the following command.

```bash
git diff
```

Note that untracked files will not be shown. You have to add untracked files before they will show up.

```sh
git add -N <untracked-file>
```

You can also see a summary of what has changed with `--stat`

```sh
git diff --stat
```

This command is useful to check for trailing white space and merge conflict markers.

```sh
git diff --check
```

You can use this command if you've already staged your changes. This is useful before you make a commit.

```bash
git diff --staged
```
