+++
title = "Git and GitHub"

date = 2018-12-06T00:00:00
lastmod = 2020-02-21T00:00:00

draft = false  # Is this a draft? true/false
toc = true  # Show table of contents? true/false
type = "docs"  # Do not modify.

# Add menu entry to sidebar.
linktitle = "Git and GitHub"
[menu.docs]
  parent = "Fundamentals"
  weight = 25
+++

## Meta
<i class="meta-badge semester-sp19"><i class="far fa-calendar-alt fa-lg"></i>&nbsp; **Spring 2020** </i> 
<i class="meta-badge progress-full"><i class="fas fa-tasks fa-lg"></i>&nbsp; **Full** </i> 
<i class="meta-badge progress-update"><i class="far fa-clock fa-lg"></i>&nbsp; **2020-02-21** </i>

## Key Topics
<a class="meta-badge tool" href="/docs/topic-index/#e-h"><i class="fas fa-desktop fa-lg"></i>&nbsp; **GitHub**</a>

## Overview
Much of our interaction this semester outside of class will utilize GitHub.com (or just "GitHub"). GitHub is a web service that is a social network for programmers, developers, data scientists, researchers, and academics. It is also a tool for collaborating on projects, especially projects that involve writing code.

We'll use GitHub as an alternative to Blackboard, the *course management system* that students are typically familiar with. Course materials will be posted there, and GitHub's features will allow you to copy them and keep them updated as changes are made. You'll also use GitHub to submit assignments for grading, and we'll give you feedback and grades via GitHub as well.

## Git Basics
### Git
GitHub is a web application that utilizes [Git](https://git-scm.com):

> Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

Essentially, Git is a project-wide system for tracking changes to files. Think of it as Microsoft office's track changes feature on steroids - every change to every file in a directory is tracked. A directory that has tracking enabled with Git is called a **repository** or "repo" in Git-lingo.

You do no need to host files online to use Git. If you have a project saved locally (say, a doctoral thesis), you could utilize Git to version control that project without ever uploading it to the Internet. However, Git integrates seemlessly with **remote** repositories. The most well-known host of remote repos is [GitHub.com]. 

Beyond "repositories", there are a few additional terms that are specific to Git and that are helpful to know:

  * **Clone**: Make an identical copy of a repository on your local hard drive.
  * **Commit**: Approve any changes you have made to a repository.
  * **Sync**: For cloned repositories, files that have been changed need to be synced or **pushed** to GitHub.com after they are committed.

For our purposes, this is just about all you need to know about Git. If you want to learn more, [Git's 'About' page](https://git-scm.com/about) is a great place to start.

### GitHub.com
GitHub is a web service that can host projects using Git's version tracking. It is widely used by programmers, software developers, data scientists, and academics to host and collaborate projects.

GitHub is an excellent way to backup files for a project since you can "sync" changes made to a repository up to GitHub's servers. It is also an excellent way to collaborate on files with colleagues while also using Git's version tracking. Repositories can be either public (like all of the repos for our seminar) or private, which means that only people who have been given access to can view the contents of the repo. Private repos require an upgraded account, which retails for $7/month.

Students can get access to GitHub's paid services for free, however, by signing up for a [free student account](https://education.github.com). This will give you access to private repositories for as long as you are a student. GitHub also provides this free upgrade service to educators, which is how our classes have private repositories.

## The Workflow of Git and GitHub
The typical approach to versioning for many students is manual. For a hypothetical class response paper, it might look something like this:

```{r echo=FALSE, fig.align="center", out.width = '50%'}
knitr::include_graphics("images/gitFlow01.png")
```

The author made an initial copy of the paper, and then used a haphazard and inconsistent approach for naming subsequent copies of the paper. We can presume that changes were made in a linear fashion, though it is easy to make changes to, say, `First Response Paper 2.doc` after `First Response Paper 3.doc` has been created and edited.

### Commits

Instead of saving copies of their hypothetical paper, a student using GitHub could write the paper in a single document, **commiting** their changes as they progress to take "snapshots" of their progress. These snapshots contain information on changes the student has made, tracked line-by-line. So, at each point in which a new document would have been created in the typical workflow, a student using GitHub would simply **commit** their changes:

```{r echo=FALSE, fig.align="center", out.width = '95%'}
knitr::include_graphics("images/gitFlow02.png")
```

Git provides a number of useful features beyond simply tracking changes. Each commit is accompanied a **message**. These messages must have a short summary that appears on GitHub and can also have a longer description that can be used to describe in detail what changes are being applied with a specific commit:

```{r echo=FALSE, fig.align="center", out.width = '95%'}
knitr::include_graphics("images/gitFlow03.png")
```

Messages, combined with the changes that are tracked, allow users to trace the development of a single document or an entire project overtime:

```{r echo=FALSE, fig.align="center", out.width = '95%'}
knitr::include_graphics("images/gitFlow04.png")
```

This means that, if necessary, the project can also be rolled back to an earlier period. Finally, users can **sync** their commits with GitHub.com, hosting their changes and their data in a way that protects them against certain types of computer failures and also allowing them to easily share their work with others.

### More About Repositories
Users of GitHub.com adhere to a couple of norms with their repositories that are worth knowing about. Repositories cannot have spaces in their names (much like objects in `R`), so the naming conventions that we will discuss in relation to `R` this semester all apply to GitHub as well!

Public GitHub repositories also contain (typically) at least three core files:

  1. A **license** file - since the data is out there for public consumption, it is important to think about how that data is licensed. The norm among GitHub users has been to use open source licenses, which let others edit and adapt your work. There are a range of [licenses](http://choosealicense.com) that are commonly used on GitHub.

  2. A **README** file - this describes the purpose and content of the project.

  3. A **.gitignore** file - this stops certain types of files from being swept up by GitHub when a user syncs their files with a server.

When you clone your repositories, you will be prompted to save them on your computer. There are a number of ways in which this process can introduce sources for trouble down the road. The principle way that I have seen students run into problems with GitHub is by storing repositories on cloud storage services like Dropbox or Google Drive. In order to avoid any issues, I advise against storing GitHub repositories in an area of your computer that syncs with a cloud service.

## GitHub Issues
GitHub has a powerful tool for interaction called [Issues](https://help.github.com/articles/about-issues/). These can be accessed by opening a repository and then clicking on the "Issues" tab. Issues can be "opened" by anyone with access to the repository. They allow for a conversation to occur in the form of messages posted within the Issue itself. Files can be attached to Issues, and the messages can contain Markdown formatting. Once the conversation is complete, issues can be marked as "closed", which moves them into a secondary view on the website so that they are archived.

We'll use issues for both assignment feedback and grading. Please keep up with issues are they appear, and feel free to follow-up with specific questions about your grade or the assignment feedback in the Issue conversation. Once you are satisfied, please mark the issue as closed.

## GitHub Desktop
[GitHub Desktop](https://desktop.github.com) is a tool that allows you to easily clone repositories hosted on GitHub, commit changes to them, and then sync those changes up to the website. You can also create new repositories, however this is not task you will have to do this semester. GitHub Desktop is not a fully functional desktop version of GitHub. For our purposes, it is important to note that the Desktop application will not let you easily identify when repositories have been updated by other users, view Wikis associated with repositories, or view Issues.

## Learning More
GitHub has a [resources page](https://help.github.com/articles/good-resources-for-learning-git-and-github/) with links to websites that are great for helping you learn more about how Git and GitHub work! The next chapter also has some additional GitHub and Git information.

One particularly great [tutorial](https://try.github.io/) walks you through the command line process for creating and using a git repository. Even if you do not want to use Git via the command line, the tutorial does an *excellent* job of describing the logic and sequence behind the Git workflow.