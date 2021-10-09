---
title: "Repeating keys stopped working in macOS"

tags: [keyboards, macos]
categories: [software engineering]
---

I'm not sure why this happened, but at some point I lost the ability to hold down on a key to repeat them.

To solve this, run the following command in a terminal. You may need to restart the terminal for it to work.

```sh
defaults write -g ApplePressAndHoldEnabled -bool false
```
