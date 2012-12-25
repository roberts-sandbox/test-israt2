---
layout: post
title: "Your Git Answers"
date: 2:30 AM 12/12/2012
comments: true
categories: QA
---

# Collected answers for your [git](http://git-scm.com/) questions

For the past couple of years, I am actively using git for my personal projects. It's an extremely helpful tool compare to any of the version controls I have used like ClearCase, SVN etc. Most of the people who works with git is well verse with the commands rather than sticking with a GUI client. Well, except GitHub (for Windows) and few IDE plugins, fundamentally Git does not have any good UI like SVN or Clearase. [You can see a few here](http://git-scm.com/download/gui/win). Stackoverflow is an amazing place where you can find as many answers for your questions on git. Here I am trying to consolidated the usual suspect which I bumped in to several times and had to fire Google to get an answer. Feel free to send me a [pull request](https://help.github.com/articles/using-pull-requests) if you find more things need to me added in to this.

I am not supposed to cover the fundamentals like git init, git add, git commit, git push etc. I hope you know the basic workflow of using git.

##.gitignore
It's important to have a `.gitignore` file in your respository. A simple `git add .` adds the whole contents in the folder to your current repository. a `.gitignore` It helps to avoid the unnecessary (like compiler output etc.) to get added in your repository. Interestingly Github maintains a repository which contains the templats of .gitignore files for several languages available. You will have to customize it if your project using multiple languages or it hinders you from adding the required files. Basically it works for typical cases. Clone, keep and use it whenever required.

[github/gitignore](https://github.com/github/gitignore)

##Github for Windows
It helps you to Clone,Repositories,Browse History,Commit Changes,Branch Code and Share on GitHub.com (as advertised on their website). The Metro style UI is really beautiful and this utility is very handy to work with GitHub.

[Github for Windows](http://windows.github.com/)

##Undoing the modifications

You can use `git checkout` command for this. See the example below
`git checkout -- <file-name>`
