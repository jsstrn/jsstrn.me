---
title: "How to setup a local web server with a Synology NAS server"

tags: ["nas", "synology"]
categories: ["technology"]
---

Go to `Package Center` and install `Web Station`. Now you should be able to see a default webpage when you visit `http://<your-ip-address>` or `http://<server-name>.local` (the default port is `80`).

To edit the webpage, go to the `web` directory in your `File Station`.

Note that the website is only accessible within your local network. If you want to be access it via the internet you'll need to setup DDNS.
