---
title: "Add aliases to Git commands"
summary: "Here's how to add aliases to common Git commands"

tags: ["git"]
categories: ["software engineering"]
---

To create an alias for `git checkout`.

```bash
git config --global alias.co checkout
```

Instead of `git checkout`, you can now run

```bash
git co
```

Some common aliases to consider adding

```bash
git config --global alias.co checkout
git config --global alias.st "status --short"
git config --global alias.lg "log --oneline --graph"
git config --global alias.uncommit "reset --soft HEAD~1"
```

To see the list of aliases in your Git configuration

```bash
git config --list | grep alias
```

If you want to add this as an alias you will need to add `!` to qualify it as a full Bash command

```bash
git config --global alias.alias "!git config --list | grep alias"
```

If you use dotfiles, you can add all your aliases directly to your `.gitconfig` file.

```sh
[alias]
	br = branch
	cm = commit -m
	co = checkout
	st = status
```
