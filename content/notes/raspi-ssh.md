---
title: "SSH into a Raspberry Pi"
summary: "How to SSH into a Raspberry Pi"

tags: ["raspberry pi", "ssh"]
categories: []
---

First, we have to assign a static IP address to the Raspberry Pi on your home router. Most home routers will allow you to do this. Read your home router manual to learn how to do this. 

Now you can access the Raspberry Pi remotely via SSH `ssh <username>@<ip-address>`

For example, if you gave `192.168.1.123` to your Pi, then you can connect to your machine like so

```sh
ssh pi@192.168.1.123
```

The default username is `pi` and the default password is `raspberry`. For security reasons, you should change your password.
