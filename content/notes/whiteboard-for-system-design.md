---
title: "The best online whiteboards for system design interviews"

tags: [interviews, tools, resources]
categories: [software engineering]
---

While there are plenty of online whiteboards available to choose from, many of them require you to sign up for an account before you can use them. This might be suitable for collaborations with teams, but adds a layer of friction for those of us who want to use it during system design interviews.

The tools I have listed are ones that are open source and do not require creating an account to use them.

## Excalidraw

[Excalidraw](https://excalidraw.com/) is a barebones online whiteboard tool with limited features. You don't need to sign up to use it and can immediately share your whiteboard with collaborators.

One useful addition that you should do is to add the [System Design Components](https://libraries.excalidraw.com/?target=_excalidraw&referrer=https%3A%2F%2Fexcalidraw.com%2F&useHash=true&token=6MlslDbfgXpglogHz4mIe&theme=dark&sort=default#rohanp-system-design) by Rohan Pithadiya. There are many other drawing components that you can add from the their public library.

Other features include, keyboard shortcut, a light and dark theme, exporting your drawings in `.excalidraw`, `.png`, or `.svg` file formats.

Excalidraw is an [open source](https://github.com/excalidraw/excalidraw) software built in Reat and written in TypeScript. They also have a [Docker image](https://hub.docker.com/r/excalidraw/excalidraw) available so you can host your own instance under your own domain. There's even an [npm package](https://www.npmjs.com/package/@excalidraw/excalidraw) so you can use Excalidraw as a React component in your projects.

## Diagrams.net (previously Draw.io)

[Diagrams.net](https://app.diagrams.net/) is an excellent tool that's suitable for all sorts of diagrams including system design, flowcharts, UML diagrams, and more.

They do require you to sign in to your Google Drive in order to collaborate with others. This isn't ideal. If you can share your screen during your interview then this solution works well for you. Just keep in mind that you cannot share your screen on Pramp, so this solution is not suitable.

Diagrams.net has a lot more features then Excalidraw. You can create your own custom shapes and add them to your scratchpad. You can also add more shapes to your current collection.

For offline use, there is a [desktop version](https://github.com/jgraph/drawio-desktop/releases) that's available for pretty much every operating system. On a Mac, simply use Homebrew to install the app.

```sh
brew install --cask drawio
```

There's even an [extension](https://marketplace.visualstudio.com/items?itemName=hediet.vscode-drawio) for VS Code so you can draw diagrams within the code editor. All you need to do is install it and create a file with a `.drawio` extension (e.g. `diagram.drawio`). Now you can commit your editable diagrams to your code repository.

Now you can see why Diagrams.net is my personal favorite tool.
