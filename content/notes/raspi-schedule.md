---
title: "Schedule a Cron job on Raspberry Pi"
summary: "How to schedule a Cron job on your Raspberry Pi"

tags: ["raspberry pi", "cron"]
categories: []
---

It is often recommended to install updates before installing other packages, we can create a Cron job that will run these commands on a daily basis.

List existing Cron jobs

```sh
crontab -l
```

Create a new Cron job

```sh
crontab -e
```

Now add this line to the `crontab` which will run daily at midnight

```sh
0 0 * * * sudo apt update && sudo apt --yes upgrade
```

## Reference

- [Scheduling tasks with Cron](https://www.raspberrypi.org/documentation/linux/usage/cron.md)
