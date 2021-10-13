---
title: "Create a resume with JSON Resume"

tags: [resume]
categories: [technology]
---

Install `resume-cli` tool

```sh
npm install -g resume-cli
```

Create a new `resume.json` file

```sh
resume init
```

Validate `resume.json` to ensure it adheres to the [schema](https://jsonresume.org/schema/)

```sh
resume validate
```

Export your resume to HTML or PDF with [themes](https://jsonresume.org/themes/)

```sh
resume export --format <type> --theme <theme-name>
```

Serve your `resume.json` locally

```sh
resume serve --theme <theme-name>
```

To host your resume online, create a Gist on GitHub named `resume.json` and point to `http://registry.jsonresume.org/<your-github-username>`.
