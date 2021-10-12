---
title: "Reset changes in Git"
summary: "Reverting your changes in Git"

tags: [git]
categories: [software engineering]
---

Let's assume you have made three commits to your master branch.

```sh
A - B - C (master)
```

Move commits in C to staged with `git reset --soft B` where `B` is the commit hash.

```bash
A - B - C (master)
git reset --soft B
A - B (master)
C is in staged
```

Move commits in C to unstaged with `git reset B` where `B` is the commit hash.

```bash
A - B - C (master)
git reset B
A - B (master)
C is in unstaged
```

⚠️ Exercise caution when doing this! Remove commits in C along with any other unstaged changes with `git reset --hard B` where `B` is the commit hash.

```bash
A - B - C (master)
git reset --hard B
A - B (master)
C has been discarded
```
