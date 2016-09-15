---
layout: page
title: User's Guide
tagline: Introduction
tags: [Stata]
description:
---

This text is a companion document for **SOC 5050 - Quantitative Analysis: Applied Inferential Statistics**. It is one of four core resources for this course. The [**Syllabus**](https://github.com/slu-soc5050/Core-Documents/blob/master/syllabus.pdf) sets out core expectations and policies for the course, many of which I am required by Saint Louis University to include. The [**Reading List**](https://github.com/slu-soc5050/Core-Documents/blob/master/reading-list.pdf) contains topics, readings (both required and optional), and assignment due dates for each week. These two documents spell out what is *required* for this course.

This **User’s Guide** document is different. This is designed to help you be *successful* in this course. The idea behind a course User’s Guide is to create a reference for many of the intangible, subtle or disparate skills and ideas that contribute to being a successful researcher. In creating a User’s Guide, I draw inspiration from the work of Donald Knuth. Knuth has discussed his experiences in designing new software languages, nothing that the developer of a new language

> …must not only be the implementor and the first large-scale user; the
designer should also write the first user manual…If I had not
participated fully in all these activities, literally hundreds of
improvements would never have been made, because I would never have
thought of them or perceived why they were important…

While there is nothing particularly new about what I am writing here, and I am certainly not developing a new language for computing, the goal of the **User’s Guide** remains similar to Knuth’s experience. However, by distilling some of key elements for making a successful transition to being a *professional developer* of knowledge rather than a *casual consumer*, I hope to both improve the course experience itself and also create an environment that fosters a successful learning experience for you.

If you read through the course objectives included in the syllabus, you will note that calculating statistics is only one of the course objectives. As much as this is a statistics course, it is a course in research methods. Not just any research methods, but *high quality* research methods. Research methods are about more than methodology. Research methods are the mental habits and technical practices that make you a successful researcher. The skills and techniques that we will discuss this semester are not taught as often in graduate programs. Instead, they are often the products of "learning the hard way". These "habits of mind and habits of method" are broadly applicable across methodologies and disciplines.

### Approaching SOC 5050
Students have varying experiences learning statistics. For some, the mathematics and programming that are the foundation for contemporary quantitative methods come naturally. For others, statistics courses are an anxiety producing experience. I am fond the phrase "your mileage will vary" for describing these differences - no two students have the exact same experience taking a methods course.

#### Zen and the Art of Data Analysis
One of the biggest challenges with this course can be controlling the anxiety that comes along with learning new skills. Formulae, Markdown syntax, and Stata commands can seem like foreign alphabets at first. Debugging Stata do-files can be both challenging and a large time suck, in part because you are not yet fluent with this language. Imagine trying to proofread a document written in a language that you only know in a cursory way but where you must find minute inconsistencies like misplaced commas.

For this reason, I also think it is worth reminding you that many
students in the social sciences struggle with statistics at first. It is normal to find this challenging and frustrating. I find that students who can recognize when they are beginning to go around in circles are often the most successful at managing the issues that will certainly arise during this course. Recognizing the signs that you are starting to spin your wheels and taking either ten minutes, an hour or two, or a day away from statistics coursework is often a much better approach than trying to power through problems.

#### An Apple a Day
Being able to walk away from an assignment for a day requires excellent time management. If you are waiting until the night before or the day of an assignment’s due day to begin it, you give yourself little room for errors. I recommend approaching this course in bite size chuncks - a little each day. The most successful students do not do all of their reading, homework, and studying in a single sitting. I find that this approach not only creates unnecessary anxiety around assignments, it also dramatically limits the amount of course material you can absorb. Keep in mind that I expect the *median* student to spend approximately six hours on work for this class each week (twice the amount of in-class time).

A sample approach to the class might look something like this:

  - Monday: class
  - Tuesday: finish lab
  - Wednesday: Start problem set
  - Thursday: Finish problem set
  - Friday: First reading
  - Saturday: Second reading


#### Reading with Purpose
The book and article **reading assignments** for this course are
different from most of the other reading you will do in your graduate program because they are often very technical. Students who are most successful in this course read twice. Read the first time to expose yourself to the material, then take a break from the reading. During this first read, I don’t recommend trying to complete the example problems or programming examples. Focus on the *big picture* - what are the concepts and ideas that these readings introduce?

During the second read, try to focus in in the *details* - what are the technical details behind the big picture concepts? I recommend doing this second read with your computer open. Follow along with the examples and execute as much of them as you can. By using this second read through as a way to test the waters and experiment with the week’s content, you can come into the lecture better prepared to take full advantage of the class period. Students who follow this approach are able make important connections and focus on the essential details during lectures because it is their third time being exposed to the
course material. They are also in a much stronger position to ask
questions.

#### Active Lectures and Labs
During **lectures**, I introduce many of the same topics that your readings cover. This again is intentional - it gives you yet another exposure to concepts and techniques that are central to inferential statistics. One mistake students sometimes make is focusing on the details of *how* to do a particular test rather than focusing on *when* a test should be done. If you know when a test is needed but cannot remember how to do it in Stata, you can look this information up. Conversely, detailed notes on executing Stata commands may not be helpful if you are unsure when to use a particular test. There is no penalty in this course for not knowing how to execute a command from memory; this is what reference materials are for. The most successful students will therefore focus on *when* a particular test is warranted first before focusing on *how* to execute that test.

Getting experience with executing commands is the purpose of the **lab exercises**. Time for beginning these exercises is given at the end of each class meeting, and replication files will be posted on GitHub for each lab.

### Typefaces, Fonts, Files, and Examples

#### Typefaces and Fonts
Stata publications use a `monospaced typewriter style typeface` to refer to Stata commands (inputs) and Stata results (outputs). I take the extra step of highlighting commands with a when they are referenced in a sentence. In some documents, like lecture slides and cheat-sheets, I may highlight a command by using a to increase the visibility of the command name itself.

The `typewriter typeface` is also used to refer to filenames (e.g. `auto.dta`) or filepaths (e.g. `C:\Users\JSmith\Desktop`). Finally, we will use the `typewriter typeface` to refer to GitHub repositories (e.g. `Core-Documents`, the repository that contains this file).

Stata publications use *italicized text* to refer to text that is meant to be replaced. These references will typically appear in a `typewriter typeface` since they are often part of commands. For example, `describe varname` (with `varname` *italicized*) indicates that you should replace the text `varname` with the appropriate variable name from your dataset.

Stata publications use a sans serif typeface to refer to areas of the Stata user interface, menu items, and buttons. Stata publications also use a sans serif typeface to refer to keyboard keys (e.g. Crtl+C) where the plus sign (+) indicates that you should press multiple keys at the same time.

A sans serif typeface combined with a right facing triangle-style arrow (>) is used to refer to actions that require clicking through a hierarchy of menus or windows (e.g. File > Save).

FYI, Since you are reading this document rendered as a Markdown file, you can't see exact examples of what a sans serif typeface looks like.

#### Stata Files

There are a number of file types that are important for our use of Stata. These are all likely file types that you have never come across before, and are all discussed in greater detail in the Introducing Stata chapter (see page ).

  - `.do` - “Stata Do-files” - These are code files that contain
    commands that Stata can execute automatically. All final analyses and manipulations for research should be done via do-files to increase project documentation and reproducibility.

  -  `.dta` - “Stata Datasets” - These are the format that Stata stores tabular data in. We call these “D-T-A” files.

  - `.smcl` - “Stata Log-files” - The default file format for Stata log-files is the `.smcl` file format, which is a varient of `html`. It is pronounced “smick-el”. I recommend avoiding this file format whenever possible since only Stata can read it. Instead, save your log-files using the `.txt` file extension and the `text` option. The `.txt` file-type is a so-called “plain text” file format that can be read by an innumerable number of applications. This makes it excellent for reproducibility.

#### Other Files
We will also use a number of other types of files throughout the
semester. Some may be file types that you have come across before.

  - `.md` - “Markdown files” - These are plain text files that contain Markdown syntax (see page ). They are saved with a special file extension so that software applications and web browsers know to take advantage of the embedded Markdown syntax.

  - `.png` - “Portable Network Graphics” or “PNG files” - These are image files designed primarily for use on the Internet and on computer displays.

  - `.txt` - “Plain text files” or “Text files” - These are files that contain text without any formatting (like bold or italicized text, for example). These can be opened by a wide array of text editor applications across all major operating systems.

#### Examples
Throughout the semester, I will give you examples both in lecture slides and in an example do-file. Examples in lectures and course documents can be easily identified by their use of the `typewriter typeface`:

```Stata
. summarize mpg
    Variable |        Obs        Mean    Std. Dev.       Min        Max
-------------+---------------------------------------------------------
         mpg |         74     21.2973    5.785503         12         41
```

Examples will almost always use the file `auto.dta`, which comes pre-installed with Stata. To open it, use the `sysuse` command: `sysuse auto.dta, clear`. This allows you to easily recreate examples by minimizing dependencies within do-files.

----

##### [Back to User's Guide Cover Page]({{ base }}/pages/user-guide.html)
