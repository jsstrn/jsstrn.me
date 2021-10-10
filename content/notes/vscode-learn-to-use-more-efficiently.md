---
title: "Learn to use VS Code more efficiently"

tags: [vscode]
categories: [software engineering]
---

## Multi-cursor editing

Select your text, hit `Shift-Command-L` to select all occurences of the selection. `Command-D` to select them one at a time.

Add a new cursor above or below, `Option-Command` + `up/down` arrow keys.

Hit `Escape` key to exit multi-cursor mode.

## IntelliSense

The default shortcut key to trigger suggestions is `Control-Space` or `Fn-Control-Space`. If this does not work, try the `Option-Escape` keys.

## Line actions

To delete an entire line, hit `Shift-Command-K` or `Command-X`.

The latter works on any editor because it's the standard cut keyboard shortcut. This means the deleted line is also in your clipboard, so just `Command-V` to paste it to another line.

To move an entire line, hit `Option` + `up/down` arrow keys. To duplicate an entire line, hit `Shift-Option` + `up/down` arrow keys.

## Errors and warnings

Errors and warnings are denoted by colored squiggles in your code. You can hit `F8` key to move to the problem. Hitting `F8` again navigates to the next problem.

## Formatting

To format the current document press `Shift-Option-F`. You can also set to format on save in settings.

Open the file by hitting `Enter`. To open in a split screen hit `Control-Enter`.

## Interactive playground

VS Code has a tutorial to show some of its features. To open it, navigate to `Help` > `Interactive Playground`.
