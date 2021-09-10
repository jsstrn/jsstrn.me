---
title: "Update your Raspberry Pi"
summary: "How to update your Raspberry Pi"

tags: ["raspberry pi"]
categories: []
---

## Update your Raspberry Pi

Update the list of packages

```sh
sudo apt update
```

Then upgrade the packages

```sh
sudo apt upgrade
```

This will ask if you want to upgrade packages.

If you want to upgrade without being prompted, you can add the `--yes` flag to the command

```sh
sudo apt --yes upgrade
```
