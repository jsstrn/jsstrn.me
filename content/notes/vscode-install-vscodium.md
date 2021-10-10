---
title: "Install VSCodium instead of VS Code"

tags: [vscode]
categories: [software engineering]
---

By default, VS Code will send diagnostic data which you disable in settings. To do this, search for `telemetry` in settings and select `off` under Telemetry Level.

Another approach is to install [VSCodium](https://vscodium.com/) which contains the original open sourced binaries and has telemetry disabled by default.

For macOS, use Homebrew to install VSCodium

```sh
brew install vscodium
```
