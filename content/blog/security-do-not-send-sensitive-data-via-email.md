---
date: 2021-10-10T16:09:10+08:00
title: "Do not send sensitive data via email"

tags: [security]
categories: []
---

Sending sensitive data via email is a bad idea for several [reasons](https://www.linkedin.com/pulse/why-its-ok-send-sensitive-information-over-email-christina-harbridge).

We might be inclined to think that we can first encrypt our documents before sending them, but we soon realize that we have another problem – how do we send the password to our recipient?

Of course, we can't send the password via email. What some companies have done is to use a password that is known to the customer, like their date of birth or account number and even include the format for the password.

While this might seem like a good idea, information like your date of birth or passport number can all be retrieved through social engineering. Furthermore, using such weak passwords make them easy to crack in just a few days. By including the format, you've just sped up this process to mere seconds.

Its bad enough when companies send out sensitive documents like bank statements and investment portfolios via email, but its even worse when these companies ask _you_ to send them sensitive documents via email.

Under no circumstances should you ever do this. It does not matter if they say they are from the government, your bank, or a Nigerian Prince. An email's `sender` field can easily be spoofed making them appear to have originated from a legitimate source.

---

When I had to take out a loan from a bank they required me to send over some documents over email.

First I encrypted my documents with a passphrase that was at least 30 characters long with a mix of uppercase and lowercase letters, numbers, and symbols.

I then sent the encrypted documents via email and physically made my way to the bank to tell them the password to decrypt it. It was definitely cumbersome, but I didn't see how else to go about it as they did not have an online application form.
