---
title: "Using SSH and GPG keys"

tags: [gpg, pgp, ssh, git]
categories: [software engineering]
---

With most remote Git servers such as GitHub and GitLab, you will see both SSH and GPG keys and you might be wondering what they are used for.

## SSH keys

SSH keys are used for authenticating with the remote Git server without you requiring to key in your username and password.

**We want to associate an SSH key with your computer's identity** so generate an SSH key for each device. In the event that you lose your computer, you can revoke the SSH key and commits coming from that device will no longer be allowed.

If you replace your machine with a new one just delete the old SSH key and generate a new one. If you format your machine, you will lose your SSH key and that is fine. Just replace it with a new one.

## GPG keys

GPG keys are used to digitally sign each commit so that you can prove that the commit is actually coming from you and not someone else.

Unlike SSH keys, **we want to associate a GPG key with your identity**. So you should use the same GPG key to sign all your commits regardless of which device you're committing from.

This requires that you store your GPG key securely so that you can use them on several devices at the same time. While there are many ways to back up your GPG keys securely, I find that the most convenient way is to store them in an encrypted vault.
