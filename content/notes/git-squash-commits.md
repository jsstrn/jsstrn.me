---
title: "Squash your commits"

tags: [git]
categories: [software engineering]
---

It's not uncommon to make several commits during the course of developing your feature. When it's time to push your code you want to combine all of your commits into one logical commit.

When making pull requests and submitting code for review, it's easier for others to view all of our changes in one commit rather than have them all scattered in numerous commits. To do this, we want to squash all our commits into one commit.

First, we want to select the commits we want to squash. In this case, I've selected the last 3 commits,

```sh
git rebase -i HEAD~3
```

If Git complains that we have unstaged commits then we can either commit or stash them.

We will be presented with the selected commits in our default text editor.

```sh
pick 2082d3d Keep this commit
pick 98e5cdb Squash this commit
pick a114cad Squash this commit, too
```

To squash them, change the commits from `pick` to `squash`

```sh
pick 2082d3d Keep this commit
squash 98e5cdb Squash this commit
squash a114cad Squash this commit, too
```

Next, you will be asked to add a new commit message and delete any unwanted commit messages from the squashed commits.

We're done. Let's check our commit log before pushing our changes.

```sh
git log --oneline
git push
```

Note that if these commits had previously been pushed to your remote branch, you will need to force push them.

```sh
git push --force
```
