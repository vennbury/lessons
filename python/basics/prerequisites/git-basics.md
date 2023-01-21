---
title: Git Basics
priority: 6
---

# Git Basics

## Learning Outcomes

- The difference between git and GiHub
- Version control
- Staging and commiting in git
- Pulling and pushing for Github

<br>

## Git

Git is a version control system that allows you to track changes in any set of files. This can be thought of as Google Doc's "Revision History", where you can see the exact changes someone made at a given time stamp.
In git, instead of time frames determining our version history as is done in Google Docs, we ourselves have control of when we make a change in a file by using <b>commits</b>.

<br>

### Basic Git Commands

Let's say you want to implement version control on some group of files on your system. After installing git by following the steps outlined in the [installations lesson](http://vennbury.com/lessons/python/basics/installations#installing-git-and-github-setup), we will initialize a local git repository(or repo, which is a folder that has the ability to use git commands). To do so, we will need to:

- Open up our command line and `cd` into the folder we would like to serve as the repository and
  run the `git init` command. This will create a `.git` subdirectory that contains Git metadata for the new repository.
- Next, we will modify our files to prepare ourselves for our first <b>commit</b>. Run the command `git status` to see which files have been modified since the last <b>commit</b>.
- When ready, we will place our files in the <b>staging area</b>, which specifies which files will be included in the next <b>commit</b>. You can do so by running:

```
git add <file(s)>    # stage a set of files
git add <directory>  # stage a directory
git add .            # stage all modified files
```

- Lastly we will <b>commit</b> our changes. You can either run `git commit` which will launch your shell and prompt you to write a <b>commit</b> message or you can do it in one command by running `git commit -m "[your_message]"`.
- Run `git log` to see your <b>commits</b> in your command line listed in reverse chronological order.

<br>

## Where does Github fit in?

GitHub allows you to store your <b>commits</b> online in a GitHub repo which can be also refered to as your remote repository. This can be useful if you are working on multiple machines or working on a project with another person. You can store your <b>commits</b> on Github by <b>pushing</b> your local commits to a GitHub repository. This can be accomplished by a simple `git push` command. If some other computer <b>pushed</b> new commits to the repository, you can download those changes by going into your local repository and <b>pulling</b> them. This is similarily accomplished with the `git pull` command. You will get some practice with <b>pushing</b> and <b>pulling</b> in the next lesson.

<br>

## Knowledge Check

- Why is version control useful?
- What is a repository? What's the difference between a local and remote repository?
- Why do we need to stage changes in git?

<br>

## Additional Resources

- Learn what is [Git and Github](https://content.red-badger.com/resources/what-is-git-and-github).
- [Git cheatsheet](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet).
