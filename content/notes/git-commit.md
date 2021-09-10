---
title: "View changes before committing"
summary: "Review code changes before staging and committing"

tags: ["git"]
categories: ["software engineering"]
---

Avoid blindly staging code with `git add --all` or `git add .` as you may accidentally stage and commit code that you didn't intend to.

I prefer to use `--patch` or `-p` when adding code to staging. This allows you to go through your changes and review them by hunks.

```bash
git add -p
```

Since new files are not tracked they will not show up in `--patch` so you have to use `--intent-to-add` or `-N` to track those files before you can use `--patch`.

```bash
git add -N <new-filename>
git add -p
```

You will see changes marked with `+` or `-` to indicate if code has been added or deleted. You'll be prompted as such.

```bash
(1/1) Stage this hunk [y,n,q,a,d,e,?]?
```

Typically, you reply with `y` to stage the hunk or `n` to ignore it. Sometimes we want to stage the entire file without looking at the remaining hunks in the file, we can do this with `a`. This is useful for files like `package-lock.json`.

We can manually edit `e` which lines to add or remove in each hunk. When in edit mode you will make your changes in `vim`. To remove `'+'` lines just delete them. To remove `'-'` lines, just change them to `' '`.

Use `?` to display this help screen if you ever forget what the commands stand for.

```bash
y - stage this hunk
n - do not stage this hunk
q - quit; do not stage this hunk or any of the remaining ones
a - stage this hunk and all later hunks in the file
d - do not stage this hunk or any of the later hunks in the file
e - manually edit the current hunk
? - print help
```

Once you have reviewed all your changes. You can commit your changes as usual.

```bash
git commit -m "Some meaningful commit message"
```
