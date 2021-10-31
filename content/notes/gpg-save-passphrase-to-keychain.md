---
title: "Save your GPG key passphrase to Keychain"

tags: [gpg]
categories: [software engineering]
---

If you use your GPG key to sign your commits you will have to key in your passphrase each time you make a new commit. You can save your passphrase to Keychain with the help of Pinentry Mac.

Install `pinentry-mac` from Homebrew

```sh
brew install pinentry-mac
```

Open the configuration file to your `gpg-agent` located at `~/.gnupg/gpg-agent.conf` with `vim` or your favorite editor. 

```sh
vim ~/.gnupg/gpg-agent.conf
```

Add this line to set your `pinentry-program` to `pinentry-mac`

```sh
pinentry-program /usr/local/bin/pinentry-mac
```

Restart `gpg-agent`

```sh
gpgconf --kill all
```

Now when you are prompted to type in your passphrase for your GPG key, it will use Pinentry Mac with the option to "Save in Keychain."

That's it. You should not need to key in your passphrase the next time.
