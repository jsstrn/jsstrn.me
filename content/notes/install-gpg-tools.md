---
title: "Installing GPG Suite on macOS"

tags: [gpg]
categories: [software engineering]
---

You don't actually need to install GPG Suite. You can access all your GPG keys via the `gpg` command line tool via your terminal.

Installing GPG Suite gives you the GPG Keychain which makes it easier for you to view all your keys and to store your passphrase in the keychain so that you don't have to keep typing it in all the time.

You can either download and install [GPG Suite](https://gpgtools.org/) directly from their website or via Homebrew.

Typically, I prefer to install applications via Homebrew

```sh
brew install --cask gpg-suite-no-mail
```

However, after installation I encountered an issue where the `gpg` and `gpg-agent` versions would not match and this created problems for me when I try to sign my Git commits.

If you encounter this issue as well, you have to uninstall the version from Homebrew and directly install it from [GPG Suite](https://gpgtools.org/).

During the installation process remember to remove GPG Mail.
