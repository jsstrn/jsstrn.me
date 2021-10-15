---
title: "Multiple cursors with Vim"

tags: [vim]
categories: [software engineering]
---

Multiple cursor before the first character of the next couple of lines

```txt
first item
second item
third item
last item
```

1. Move your cursor to the first character in the first line.
2. Press `v` to enter into visual mode
3. Press `j` until all the lines you want to edit have been selected
4. Press `I` to enter into insert mode at the beginning of the line
5. Type the text you want and hit `Escape`

```txt
My first item
My second item
My third item
My last item
```
