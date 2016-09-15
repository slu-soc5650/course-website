---
layout: page
title: User's Guide
tagline: Introduction to GitHub
tags: [GitHub]
description:
---

This wiki is hosted on [GitHub.com](https://github.com). We've added a quick introduction to Git and GitHub here since we know many of you have not been exposed to GitHub before.

### Git
GitHub is a web application that utilizes [Git](https://git-scm.com):

> Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

Essentially, Git is a project-wide system for tracking changes to files. Think of it as Microsoft office's track changes feature on steroids - every change to every file in a directory (a "repository" or "repo" in Git-lingo) is tracked. You do no need to host files online to use Git. If you have a project saved locally (say, a doctoral thesis), you could utilize Git to version control that project without ever uploading it to the Internet.

For our purposes, this is just about all you need to know about Git. If you want to learn more, [Git's 'About' page](https://git-scm.com/about) is a great place to start.

### More Git-lingo
Beyond "repositories", there are a few additional terms that are specific to Git and that are helpful to know:

  * **Clone**: Make an identical copy of a repository on your local hard drive.
  * **Commit**: Approve any changes you have made to a repository.
  * **Sync**: For cloned repositories, files that have been changed need to be pushed to GitHub.com after they are committed.

### GitHub
GitHub is a web service that can host projects using Git's version tracking. It is widely used by programmers, software developers, data scientists, and academics to host and collaborate projects.

GitHub is an excellent way to backup files for a project since you can "sync" changes made to a repository up to GitHub's servers. It is also an excellent way to collaborate on files with colleagues while also using Git's version tracking. Repositories can be either public (like all of the repos for our seminar) or private, which means that only people who have been given access to can view the contents of the repo. Private repos require an upgraded account, which retails for $7/month.

Students can get access to GitHub's paid services for free, however, by signing up for a [free student account](https://education.github.com). This will give you access to private repositories for as long as you are a student.

### GitHub Repositories
Users of GitHub adhere to a couple of norms with their repositories that are worth knowing about. Repositories cannot have spaces in their names (much like objects in `R`), so the naming conventions that were discussed in Seminar 01 all apply to GitHub as well!

Public GitHub repositories also contain (typically) at least three core files:

  1. A **license** file - since the data is out there for public consumption, it is important to think about how that data is licensed. The norm among GitHub users has been to use open source licenses, which let others edit and adapt your work. There are a range of [licenses](http://choosealicense.com) that are commonly used on GitHub.

  2. A **README** file - this describes the purpose and content of the project.

  3. A **.gitignore** file - this stops certain types of files from being swept up by GitHub when a user syncs their files with a server.

Another norm is to write using a [markup language](https://en.wikipedia.org/wiki/Markup_language) known as [Markdown](https://daringfireball.net/projects/markdown/). Markup languages allow users to specify exactly how they want their text to appear when it is parsed and processed by special software. This is different from, say, Microsoft Word, which is known as a "what you see is what you get" or **WYSIWYG** editor, which uses a graphical interface for constructing documents.

### Storing GitHub Repositories
When you clone your repositories, you will be prompted to save them on your computer. There are a number of ways in which this process can introduce sources for trouble down the road:

  1. External media - storing data on devices like thumb drives or external hard drives can be a part of a [backup workflow](protecting-your-work.html). However, I have seen issues where this has appeared to contribute to sync errors with GitHub Desktop, particularly on Windows.
  2. Cloud storage services (Dropbox, Google Drive, etc.)  - like external drives, these services can be a part of a [backup workflow](protecting-your-work.html). However, like external drives, I have seen issues whee this has to contribute to sync errors with GitHub Desktop.

In order to avoid any issues, I suggest storing GitHub repositories on your computer's hard drive and not a thumb drive or other external device. Make sure your are saving your files in a place not backed up to Dropbox or another cloud storage service.

### Learning More
GitHub has a [resources page](https://help.github.com/articles/good-resources-for-learning-git-and-github/) with links to websites that are great for helping you learn more about how Git and GitHub work!

----

##### [Back to User's Guide Cover Page]({{ base }}/pages/user-guide.html)
