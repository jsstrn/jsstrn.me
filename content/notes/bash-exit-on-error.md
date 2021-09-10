---
title: "Exit a Bash script on error"
summary: "How to exit a Bash script when any command fails"

tags: ["bash"]
categories: ["software engineering"]
---

If we want a Bash script to stop executing the rest of the script when one of the commands fail, we can simply add `set -e` to the top of our script.

```bash
set -e
```
