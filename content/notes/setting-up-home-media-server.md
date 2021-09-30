---
title: "Setting up a home media server"

tags: ["nas", "raspberry pi"]
categories: ["software engineering"]
---

## NAS server

If you have a NAS server, you can install [Plex](https://www.plex.tv/) or [Emby](https://emby.media) as your media server. Both Plex and Emby have [clients](https://jellyfin.org/clients/) for Apple TV and other devices.

## Raspberry Pi

If you have a Raspberry Pi, its relatively simple to turn it into a media server with [OSMC](https://osmc.tv/) and connect it directly to a TV. The downside is that you'll need to use a keyboard to navigate around. 

## DIY

The new kid on the block is Jellyfin – an open source fork of Emby.

To install Jellyfin on a Raspberry Pi, you can follow instructions for [Debian](https://jellyfin.org/docs/general/administration/installing.html#debian).

There's even instructions to install Jellyfin on a Synology NAS server with [Docker](https://jellyfin.org/docs/general/administration/install/synology.html). Just keep in mind that you'll need to be on [DSM 7](https://www.synology.com/en-us/dsm/packages/Docker?os_ver=7.0&search=docker).

They support numerous [clients](https://jellyfin.org/clients/), except for Apple TV. For that you have to access your content with third-party applications like Infuse or MrMC.
