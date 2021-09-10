---
title: "Which shebang to use to run Bash scripts?"
summary: "Add a shebang to the top of your Bash scripts"

tags: ["bash"]
categories: ["software engineering"]
---

This two-characters sequence `#!` is called a shebang. It is used in shell scripts to determine which interpreter should be used to run the script.

It's a good idea to include a shebang `#!` at the top of a Bash file. This is so that the sript runs correctly regardless of what shell the user is running. 

For example, if a user is using the zsh shell, the script would default to zsh syntax instead of the intended bash syntax. Adding a shebang prevents this issue.

This also means you don't have to include the `.sh` file extension. 

```bash
#!/usr/bin/env bash
```

Reference: [What is the preferred bash shebang](https://stackoverflow.com/questions/10376206/what-is-the-preferred-bash-shebang)
