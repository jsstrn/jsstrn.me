---
date: 2021-10-01T01:26:29+08:00
title: "Goodbye 1Password"

draft: true

tags: ["password management"]
categories: ["technology"]
---

I've been using 1Password since 2013 and had paid for both their macOS and iOS apps. They've recently moved to a subscription model which I have no problems paying for. Unfortunately, there are some major issues with their new product.

## Online database

Previously, we had a choice as to where we wanted to store our password vaults. We could choose any of the major cloud storage solutions like Dropbox, Google Drive or iCloud Drive.

In fact, there was a nifty tool that allowed us to sync between devices as long as they were both on the same network. This meant that we didn't even need to store our vaults on an external cloud service.

With the move to 1Password 8 they are essentially forcing users to move all our vaults to their online database.

## Poor import support

It seems like 1Password wants to make it difficult for people to switch to using 1Password from some other password manager. They do a terrible job at importing passwords from just about any other password manager.

In contrast, importing passwords from 1Password into either Enpass or Bitwarden work just fine. They also support JSON imports so file attachments are preserved.

## Desktop app powered by Electron

I've read online that many users are upset that the new desktop app will be powered by [Electron](https://www.electronjs.org/).

There may be some concerns over security [vulnerabilities](https://www.cyberscoop.com/electron-remote-code-execution-xss-slack-skype/), but even Signal uses Electron and they seem to manage [fine](https://www.theregister.com/2018/05/14/electron_xss_vulnerability_cve_2018_1000136/) so I'm not terribly concerned about 1Password's move to Electron for their desktop app.

## Conclusion

I've enjoyed using 1Password all these years, but it's time to say goodbye and move on.

{{< reply-via-email >}}
