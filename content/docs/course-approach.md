+++
title = "Approaching Coursework"

date = 2018-12-05T00:00:00
lastmod = 2018-12-05T00:00:00

draft = false  # Is this a draft? true/false
toc = true  # Show table of contents? true/false
type = "docs"  # Do not modify.

# Add menu entry to sidebar.
linktitle = "Approaching Coursework"
[menu.docs]
  parent = "Getting Started"
  weight = 4
+++

## Meta 
<i class="meta-badge semester-sp19"><i class="far fa-calendar-alt fa-lg"></i>&nbsp; **Spring 2019** </i> <i class="meta-badge progress-draft"><i class="fas fa-tasks fa-lg"></i>&nbsp; **Draft** </i> <i class="meta-badge progress-update"><i class="far fa-clock fa-lg"></i>&nbsp; **2018-12-05** </i>

## Overview

Students have varying experiences learning computational techniques. For some, the math and programming that are the foundation for modern data science techniques come naturally. For others, being introduced to these concepts can be an anxiety producing experience. I am fond the phrase "your mileage will vary" for describing these differences - no two students have the exact same experience taking a computational methods course. Like the previous chapter, some of the content below is specific to the courses ([Introduction to Geographic Information Science (SOC 4650/5650)](https://slu-soc5650.github.io) and [Quantitative Analysis: Applied Inferential Statistics (SOC 4930/5050)](https://slu-soc5050.github.io)) I teach at [Saint Louis University](https://www.slu.edu), the general outlook on approaching data science work that I describe below is hopefully applicable in a far wider arena.

## Zen and the Art of Data Analysis
One of the biggest challenges with this course can be controlling the anxiety that comes along with learning new skills. `R` syntax, GIS terms, LaTeX commands, and Markdown can seem like foreign alphabets at first. Debugging `R` syntax can be both challenging and a large time suck, in part because you are not yet fluent with this language. Imagine trying to proofread a document written in a language that you only know in a cursory way but where you must find minute inconsistencies like misplaced commas.

For this reason, I also think it is worth reminding you that many students in the social sciences struggle with computational methods at first. It is normal to find this challenging and frustrating. I find that students who can recognize when they are beginning to go around in circles are often the most successful at managing the issues that will certainly arise during this course. Recognizing the signs that you are starting to spin your wheels and taking either ten minutes, an hour or two, or a day away from computational coursework is often a much better approach than trying to power through problems.

Data analysis therefore requires a certain mindfulness. I mentioned in the [Preface] that much of what this book covers are "habits of mind and habits of method". These mental habits extend past being able to recognize that frustration is setting in. They also include the mental habits needed for [Getting and Staying Organized] and strategies for [Getting Help] as you navigate the inevitable errors that come with learning new analytically skills.

## Getting and Staying Organized
Doing data science work, and having the space to step away for a day as the last section suggests, requires discipline and organization. Similarly, computational coursework can demanding not just because it is complex but because the courses often have a number of moving pieces that you need to keep track of. Being mindful of this challenge from the beginning, and taking steps to plan for it, is an important part of this course. 

### Keeping Track of Where You Are
Students who have some system for tracking their work and creating to-do lists are often the most successful in this course, not because they have a fundamentally better grasp on the content but because they simply are more organized. If you have never thought particularly hard about how you manage tasks, now is an excellent time to start doing so. You do not need fancy computer software to accomplish this, though there are an array of possibilities if you do want to use software to keep yourself organized. A legal pad or a notebook can be just as effective as a $50 to-do list manager. The point is, do *something*!

I am fond of recommending the [**Getting Things Done**](http://gettingthingsdone.com) methodology to students as part of thinking more holistically about staying organized. The website [Lifehacker](https://lifehacker.com) posted an [excellent introduction to GTD](https://lifehacker.com/productivity-101-a-primer-to-the-getting-things-done-1551880955) that is a great way to get a sense of how it works and find additional resources for implementing it. 

The GTD website has a [great list of software](http://gettingthingsdone.com/common-tools-software/) for those of you looking for a to-do list application. One that isn't listed that I use for collaborating with my student research team is [Trello](https://trello.com), a freemium website that allows you to create simple to-do lists. It isn't sophisticated enough for implementing GTD, but it is more than sufficient for managing to-do lists related to this course.

### Managing Course Materials
For both courses covered by this book, materials will be disseminated in physical and digital form. The topic of keeping digital materials organized is the subject of the next chapter [Protecting Your Work]. The physical handouts and materials that we'll give out will all come three hole punched, and you are expected to purchase a three-ring binder for this course. I give out enough handouts that, without a binder, it becomes difficult to keep track of where handouts are located. I have watched students spend more time looking for the handout than it takes to find the answer to their question once they have the handout itself.

There are two recommended ways to keep your binder tidy. One is to organize by lecture. There are sixteen lectures worth of handouts in both courses (not including the course preview and the final research conference session), so two sets of dividers (which often come in packs of eight) should be sufficient. The other way to organize handouts is by topic. We hand out a number of different types of documents that could be organized thematically like so:

1. Syllabus and reading list
2. Workflow diagrams
3. `R` function sheets
4. ArcGIS process sheets (SOC 4650/5650 only)
5. LaTeX command sheets (SOC 4930/5050 only)
6. Sample outputs
7. Exercise handouts
8. Lab handouts
9. Problem set handouts

Since there are approximately eight different types of handouts in each class, a single package of dividers should be sufficient for this approach to organizing them.

I don't think that one way of organization, thematically or temporally, is inherently better or worse than the other. In large part it comes down to how *you* like to organize information. After all, learning how to process and organize information in a way that works for you is the most important takeaway here.

## Staying Current
Course content is maintained both on the respective course websites ([Quantitative Analysis](https://slu-soc5050.github.io) and [GIS](https://slu-soc5650.github.io)) and GitHub organizations ([Quantitative Analysis](https://github.com/slu-soc5050) and [GIS](https://github.com/slu-soc5650)). Course materials are available throughout the semester and after the course is done. This creates two challenges. First, for all students, attention must be paid to when updates are pushed to GitHub and the course website. This is particularly true for content updated *after* a lecture. Second, for students who like to work ahead, care must be taken to ensure that you are working off of materials for the current semester and not the last semester the course was taught. There are two ways in which I help communicate the status of course content - badges and Slack.

### Badges
I use badges on both the GitHub `README.md` files in individual lecture repositories and on individual lecture webpages to signal which semester the content is current for and what stage of development the content is in. These badges are used not just because they are effective but as part of a more general socialization into data science software development, where badges are used to signal development status on `R` package GitHub repositories. For example, the [`ggplot2`](https://github.com/tidyverse/ggplot2) `README.md` file looks like this:

There are four badges in total, all of which sit under the `ggplot2` package name. We can see from the first two badges that [continuous integration services](https://en.wikipedia.org/wiki/Continuous_integration) are used, and that `ggplot2` is only passing its tests on one of them. The third badge indicates that the built-in tests for `ggplot2` test 74% of the package's code. We can also see from the fourth badge that the current version of the software on CRAN is version `2.2.1` (as of December, 2017). Details like these are not critical when you are first learning to use `R`, but they grow more important as your data science skills progress.

We use the following badges for our course repositories and on the course websites:

Here is an example of how the badges look on a course repository. As of January 2018, the `README.md` associated with the [`Core-Documents` repository](https://github.com/slu-soc5050/Core-Documents) for [Quantitative Analysis](https://slu-soc5050.github.io) looked like this:

The `README.md` badges, from left to right, represent the following:

1. **semester**: the contents are current for the Fall 2017 semester 
2. **release**: the contents have been updated since they were first released to students
3. **version**: the version number of the repository (see [Versioning] below) is `v17.4.2`
4. **last commit**: the last time the repository was edited was the day the screenshot was taken
5. **repo size**: the repository size is 2.46 megabytes (MB, see [this article](https://www.computerhope.com/issues/chspace.htm) for details on what computer disk drive size measurements mean)

Here is an example of how the badges look on a course website. As of January 2018, the [Course Preview page](https://slu-soc5650.github.io/course-preview) for [GIS](https://slu-soc5650.github.io/) looked like this:

From these three badges, we can see that the webpage is current for the Spring 2018 semester and that it is the full release - no additional updates to the site are planned. Finally, we can see the date on which the page was last updated - December 29, 2017.

### Versioning
The versioning system used on course repositories is meant to emulate the release system used for data science software. Software development increasingly takes place on a website called [GitHub.com]. GitHub includes tools for packaging a repository at particular points in time. The release system allows developers to identify how an `R` package, for instance, has changed over time. This is important for reproducibility. For instance, you can see this example of the [release history for `ggplot2`](https://github.com/tidyverse/ggplot2/releases/tag/v2.2.0):

The package's developers use the release system to document what has changed. We will emulate this with the `Core-Documents`, lecture, and `finalProject` repositories. For example, here is the release documentation for [SOC 4650/5650 `Core-Documents` repository](https://github.com/slu-soc5650/Core-Documents): 

If you want to see what has changed over the course of the semester in a course's repositories, you can use the release notes to compare different versions. These notes are also stored in the `NEWS.md` file for each repository. The use of both releases and a `NEWS.md` file is a common way to document changes on GitHub. For example, you can see look at the [`NEWS.md` file for `ggplot2`](https://github.com/tidyverse/ggplot2/blob/master/NEWS.md), which will mirror the [release notes](https://github.com/tidyverse/ggplot2/releases) for the package. 

In software development, [version numbers](https://en.wikipedia.org/wiki/Software_versioning) are used along with releases to make it easy for end users to keep track of how releases have progressed. In the picture above of the `ggplot2` package's `README.md` (see [Badges]), one of the badges indicated the version of the software that was available via CRAN - `2.2.1`. The initial `2` is what is known as the major release number. Major releases typically represent large changes to the software. The second number, also a `2` in this case, represents the minor release number. Minor releases introduce fewer changes and may be aimed more at fixing issues. Finally, the `1` represents the patch release number. Patch (or maintenance) releases are aimed exclusively at fixing bugs and issues.

For the course, version numbers will also have three parts. From left to right, the first pair of digits represents the year of the current course offering, the second pair represents whether it the development status is (`1`) draft, (`2`) lecture, (`3`) full, and (`4`) updated, and the final number represents maintenance changes that do not rise to a change in the development status. For example, `v18.1.1` would represent the initial maintenance release for the 2018 version of a course that is in the draft development stage.

If you see a version number like `v18.1.1.9000` in `NEWS.md`, the notes will be tracking changes that have not been incorporated into an official release yet. The use of the `9000` designation follows [common practice in the `R` community](http://r-pkgs.had.co.nz/release.html).

### Discourse
TBA