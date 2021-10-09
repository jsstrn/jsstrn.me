---
title: "Limit number of open editors in VS Code"

tags: [vs code]
categories: [software engineering]
---

We can limit the number of open editors in VS Code by configuring the following in settings: 

- `workbench.editor.limit.enabled: true` – enable editor limit; default is `false`
- `workbench.editor.limit.value: 1` – set number of open editors; default is `10`
- `workbench.editor.limit.perEditorGroup: true` – allow side-by-side panels; default is `false`
