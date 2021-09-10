---
title: "Useful Vim commands"
summary: "A list of the most commonly used Vim commands"

tags: ["vim"]
categories: ["software engineering"]
---

## Settings

`:set number` – show line numbers

## Modes

`Esc` – command mode (default mode)

`i` – insert mode (before cursor)

`a` – insert mode (after cursor)

`v` – visual mode to select text to `y` (yank) or `d` (delete) text

## Quiting Vim

`:q` – quit

`:q!` – quit without saving

`:wq` – save and quit

`:ZZ` – save and quit

## Undo and redo

`u` – undo the previous command

`U` – undo the whole line

`Ctrl + R` – redo the previous command

## Copy and paste

`yw` – yank (copy) a word

`yy` – yank (copy) the entire line

`y$` – yank from cursor position to end of line

`yG` – yank from cursor position to end of file

`p` – to put or paste the text that was copied or deleted

## Delete

`x` – delete a character

`dw` – delete word

`dd` – delete line

`d$` – delete from cursor to end of line

`cw` – change word; this will delete the word and put you in `insert` mode

## Navigation

`h` – move left

`l` – move right

`j` – move down

`k` – move down

`0` – move to start of line

`$` – move to end of line

`nG` – move to line number where `n` is the line number (e.g. `54G` goes to line 54)

`[[` – move to start of file

`]]` – move to end of file
