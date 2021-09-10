---
title: "Assign a .local domain to a Raspberry Pi"
summary: "How to assign a <code>.local</code> domain to your Raspberry Pi"

tags: ["raspberry pi"]
categories: []
---

First, install [Avahi](https://www.avahi.org/) on your Raspberry Pi

```sh
sudo apt-get install avahi-daemon
```

Now you can access your Raspberry Pi via its hostname `raspberrypi.local` instead of its IP address. You can also change the hostname (see reference).

```sh
ssh pi@raspberrypi.local
```

## Reference

- [How (and Why) to Assign the .local Domain to Your Raspberry Pi](https://www.howtogeek.com/167190/how-and-why-to-assign-the-.local-domain-to-your-raspberry-pi/)
- [How to Change Your Raspberry Pi (or Other Linux Device’s) Hostname](https://www.howtogeek.com/167195/how-to-change-your-raspberry-pi-or-other-linux-devices-hostname/)
