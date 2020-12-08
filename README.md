# Using Git with Logic Pro X

It works. Here is how.

## Disclaimer

Use at your own risk. Git isn't exactly built to be used with Logic Pro X.

## GUIDE

### Install Git

Visit the following URL and follow instructions.

https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

### Setup Git on the project

You can also use Git Desktop, SourceTree or such visual tool but these instructions are for command line use.

1. Open Terminal and navigate to project folder (btw. save your project as folder).
2. Run `git init` to setup git for the project
3. Add `.gitignore` file and insert the following lines there.

```
Project File Backups/
Undo Data.nosync/
```

This means that project backups and undo data are going to be ignored in the version control.

4. Basically you're done. After this just use Git as it's intended to be used.

## Example of using Git

In case you're not familiar with Git here is a little cheat sheet for you.

### Commit changes

When you want to save your current status of the project, you need to commit the changes. You can do this with following commands.

```git add .```

```git commit -m "tweaked the bassline"```

What happens there, it adds all the new files into the commit and applies it with a message. These messages will help you later if you want to roll back to previous version.

### Branch out new version

When you want to create new version of the current one, check out to new branch with command

```git checkout -b different-bassline```

This will create new branch called "different-bassline". Please note that you cannot use spaces or special characters in the branch names.

### Jump between versions

When you want to go any existing branch just use checkout command.

```git checkout yesterday-jamming```

PS. Master branch is usually the one that's considered to be the main branch

### Merging branches

Let's say you're happy with some new idea you've branched out from the master version and you want to bring it in. That's when you merge.

First, make sure to checkout to the branch you want to merge IN, in this case master.

Then, let's bring in that "different-bassline" with command:

```git merge different-bassline```

### Deleting branches

Sometimes you want to delete branch, then you can use

```git branch -D branch-name```

and `git branch` would just list all the branches you have

## Backing up to GitHub & Collaborating

You can also push your repository (song project) here into GitHub. From there other producers can pull it down for themselves, make their own changes etc. When you get there, feel free to ask help.


