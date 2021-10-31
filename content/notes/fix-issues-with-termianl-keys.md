---
title: "Fix issues with terminal keys"

tags: [macos, terminal]
categories: [software engineering]
---

If you encounter issues with your terminal returning odd responses to certain keys like the `Enter` key then you can use `stty` to return them to sanity.

To reset your terminal keys to sane options

```sh
stty sane
```
