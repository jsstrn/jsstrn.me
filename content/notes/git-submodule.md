---
title: "Clone a repository with submodules"

tags: [git]
categories: [software engineering]
---

Git commands are different for different versions so be sure to check your Git version.

```bash
git --version
```

Clone a repository with submodules using the `--recurse-submodules` flag. This works for Git version 2.13 or higher.

```bash
git clone --recurse-submodules <remote-repo-url>
```

If the repository has a lot of submodules, then adding the `-j8` flag will fetch up to 8 submodules in parallel.

```bash
git clone --recurse-submodules -j8 <remote-repo-url>
```

Alternatively, first clone the repository and then add the submodules. This should work regardless of your Git version.

```bash
git clone <remote-repo-url>
git submodule init
git submodule update
```

# Reference

- [How to clone including submodules](https://www.w3docs.com/snippets/git/how-to-clone-including-submodules.html)
