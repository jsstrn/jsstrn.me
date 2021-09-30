---
title: "How to connect to your Synology NAS server with SSH"

tags: ["nas", "synology"]
categories: ["technology"]
---

First, open `Control Panel` and navigate to `Terminal & SNMP`. Next, enable SSH service. Click `Apply`. Now you can SSH into your NAS with your credentials.

Open a terminal and connect to your NAS server via SSH

```sh
ssh <user>@<ip-address>
``` 

If you have set up a `.local` domain, then 

```sh
ssh <user>@<server-name>.local
```

You will be prompted for your password. 