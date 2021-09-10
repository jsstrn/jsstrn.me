---
title: "How to install Ruby on macOS"
summary: "How to install Ruby on macOS with Homebrew and rbenv"

tags: ["ruby", "rbenv"]
categories: ["software engineering"]
---

macOS comes with its own version of Ruby which will not allow you to install Gems. To start developing in Ruby, we first have to install our own version of Ruby.

It is generally recommended to use a version manager for Ruby, like `rbenv` to manage different versions of Ruby in various projects.

```bash
brew install rbenv
```

Add this line to your `.zshrc`. This will setup `rbenv` including adding `rbenv` to your `$PATH`

```bash
eval "$(rbenv init -)"
```

See list of stable Ruby versions to install

```bash
rbenv install -l
```

Install the version of Ruby that you want

```bash
rbenv install <version>
```

State which version of Ruby you want to use as the global version

```bash
rbenv global <version>
```
