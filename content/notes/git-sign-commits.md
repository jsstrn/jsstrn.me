---
title: "Sign your commits"
summary: "How to sign your Git commits with a GPG key"

tags: [git, gpg, pgp]
categories: [software engineering]
---

## Install GPG Tools

Install GPG Tools with Homebrew. This will install the GPG Keychain

```sh
brew install --cask gpg-suite-no-mail
```

## Generate a GPG key pair

If you don't have one already, you will need to create a GPG key pair. Follow the instructions to create your key pair.

```sh
gpg --full-gen-key
```

Set a strong passphrase for your private key and store it in your password manager.

Use the email address associated with your account on GitHub account. Tip you can use the `noreply` email address `username@users.noreply.github.com`.

## Add public key to GitHub

The easiest way to retrieve the public key is with the GPG Keychain. Select the key, right click and select `Copy`. Now paste this in your GitHub settings.

Your public key should look something like this

```txt
-----BEGIN PGP PUBLIC KEY BLOCK-----

-----END PGP PUBLIC KEY BLOCK-----
```

## Tell Git about your GPG key

List all your secret keys and display the key ID in long form

```sh
gpg --list-secret-keys --keyid-format=long
```

Copy the long form of the GPG key ID.

```sh
sec   4096R/<YOUR-GPG-KEY-ID> 2016-03-10 [expires: 2017-03-10]
uid                  [ultimate] YOUR NAME <youe@email.com>
ssb   4096R/42B317FD4BA89E7A 2016-03-10
```

Next, add your GPG key ID to your local Git configuration

```sh
git config --local user.signingKey <YOUR-GPG-KEY-ID>
```

Of course, you can set this globally with the `--global` flag, but it might not be a good idea to do this in case you have more than one key used for different purposes (e.g. personal and work). Best to do this on a per repository level.

## Signing your commits

To sign your commits via the terminal

```sh
git commit -S -m "Your commit message"
```

## Set commit signing by default (optional)

To sign commits by default in a local repository

```sh
git config --local commit.gpgSign true
```

Again, you could set this globally with the `global` flag, but it may not be a wise to do so if you have both personal and work projects on the same computer.

## Test to see if it all works

To check if you are now able to sign with your default key

```sh
echo "test" | gpg --clearsign
```

To use a different key append `--local-user` or `-u`

```sh
echo "test" | gpg --clearsign --local-user <YOUR-GPG-KEY-ID>
```

If it works, you should get a prompt to enter your passphrase and the corresponding hash output.

## Storing your GPG key pair

If you lose the GPG private key then you can no longer sign your commits with that key. You must remove the public key from your GitHub account and generate a new one.

To prevent this from happening, store your GPG private keys in a secure encrypted vault. You can use tools like [Veracrypt](https://veracrypt.fr/en/Home.html) or [Cryptomator](https://cryptomator.org/) to create encrypted volumes.

## Reference

- [Generating a new GPG key](https://docs.github.com/en/authentication/managing-commit-signature-verification/generating-a-new-gpg-key)
- [Signing commits](https://docs.github.com/en/authentication/managing-commit-signature-verification/signing-commits)
- [Telling Git about your GPG key](https://docs.github.com/en/authentication/managing-commit-signature-verification/telling-git-about-your-signing-key#telling-git-about-your-gpg-key)
