+++
title = "Good Enough Research Practices"

date = 2018-12-05T00:00:00
lastmod = 2019-02-18T00:00:00

draft = false  # Is this a draft? true/false
toc = true  # Show table of contents? true/false
type = "docs"  # Do not modify.

# Add menu entry to sidebar.
linktitle = "Good Enough Research Practices"
[menu.docs]
  parent = "Fundamentals"
  weight = 2
+++

## Meta 
<i class="meta-badge semester-sp19"><i class="far fa-calendar-alt fa-lg"></i>&nbsp; **Spring 2019** </i> 
<i class="meta-badge progress-full"><i class="fas fa-tasks fa-lg"></i>&nbsp; **Full** </i> 
<i class="meta-badge progress-update"><i class="far fa-clock fa-lg"></i>&nbsp; **2019-09-18** </i>

## Overview
This section introduces some of the core concepts that support sociospatial data science works. The title of the chapter takes inspiration from a recent article titled [*Good enough practices in scientific computing*](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005510) (Wilson et al. 2017). The authors note in their introduction that scientific computing advice can sometimes be both overwhelming and focused on tools that are inaccessible to many analysts. Their goal, and the goal of this text, is to de-mystify the simplest tools that enable researchers to streamline their workflows:

> Our intended audience is researchers who are working alone or with a handful of collaborators on projects lasting a few days to a few months, and who are ready to move beyond emailing themselves a spreadsheet named `results-updated-3-revised.xlsx` at the end of the workday...Many of our recommendations are for the benefit of the collaborator every researcher cares about most: their future self.

I would argue that the skills they describe are useful beyond just a few months. Indeed, most of the skills here can dramatically improve students' dissertation experiences:

> Most importantly, these practices make researchers more productive individually by enabling them to get more done in less time and with less pain. They also accelerate research as a whole by making computational work (which increasingly means all work) more reproducible. But progress will not happen by itself. Universities and funding agencies need to support training for researchers in the use of these tools. Such investment will improve confidence in the results of computational work and allow us to make more rapid progress on important research questions.

While much of what we will talk about in this text is aimed at supporting your work, there are benefits that extend beyond your dissertation or your research projects. These benefits, which include developing sustainable workflows and structuring the way you interact with your own computer, can make everyday computing practices like checking email or organizing files an easier, more structured process.

## Reproducibility

One of the mantras of this text is an emphasis on reproducibility. The unifying feature of all of the "good enough" research practices discussed below is that they contribute to a more reproducible research product.

Reproducibility is very much in vogue right now for number of reasons. [Assessments of studies in psychology](http://science.sciencemag.org/content/349/6251/aac4716)^[Open Science Collaboration, 2015. Estimating the reproducibility of psychological science. *Science*, 349(6251), p.aac4716.], for example, have found weaker on average effect sizes and far fewer statistically significant results than the initial studies reported. There have also been high profile instances of falsified research, including [research by a graduate student at UCLA](http://nymag.com/scienceofus/2015/05/how-a-grad-student-uncovered-a-huge-fraud.html). This particular instance of fraud was identified by graduate students intent on replicating the original study.

At the same time, there is a recognition that the skills necessary for producing reproducible research are not being fostered in academic disciplines and graduate programs. Thus one of the goals of this course, and this **User's Guide** in particular, is to help develop a working knowledge of many of these skills.

One challenge, however, is that reproducibility does not have a consistent definition. Some researchers use the term to narrowly refer to code that can execute without alteration on a person's computer. Others use it to refer to research designs that can be replicated by other researchers. Still others discuss reproducibility as the ability to obtain a similar set of results or draw similar inferences from identical research designs.

When we talk about reproducibility in this class. We'll be primarily concerned with **methods reproducibility**:

> the ability to implement, as exactly as possible, the experimental and computational procedures, with the same data and tools, to obtain the same results.^[Goodman, S.N., Fanelli, D. and Ioannidis, J.P., 2016. What does research reproducibility mean?. *Science translational medicine*, 8(341), pp.341ps12-341ps12.]

Methods reproducibility in statistics means that other analysts have full access to both the original data and the steps used to render those original data into a final research product, such as a set of regression models This is increasingly seen not just a matter of good research methodology, but as a matter of research ethics as well. Being able to be transparent with research decreases the potential for cases like the [fraudulent dissertation research conducted by a UCLA graduate student named Michael LaCour](http://nymag.com/scienceofus/2015/05/how-a-grad-student-uncovered-a-huge-fraud.html). It was the efforts of [two Stanford graduate students who wanted to reproduce LaCour's findings](https://fivethirtyeight.com/features/how-two-grad-students-uncovered-michael-lacour-fraud-and-a-way-to-change-opinions-on-transgender-rights/) that ultimately led to the identification of problematic work.

For statistics, methods reproducibility is derived from a number of sources. The first source is the use of **computer code** for working with data. Rather than making manual changes to tabular data in a spreadsheet application like Microsoft Excel, computer code provides detailed records of each individual alterations. Code can be used execute tasks repeatedly, meaning that errors can be easily fixed if they are discovered an hour, a day, a week, or a month later. During this semester, we'll use `R`'s programming language to execute reproducible data cleaning processes.

The second source of reproducibility in statistics is therefore derived from the **documentation** that we create to accompany our research products. These documents outline where our data originated, what specific variables mean (a codebook), what steps were taken to create specific maps (a research log), and how our data files are organized (a metadictionary).

Our code can also be used as documentation if it is written using [literate programming](https://en.wikipedia.org/wiki/Literate_programming) techniques. In `R`, these techniques produce well annotated output that "weaves" together code, output, and narrative text that describes the function of the code and the results of the output.

The third and final primary source of reproducibility in statistics is derived from our **organizational approach** to our work. Statistics projects can require many megabytes of data spread across dozens of data files, scripts, and output files. A disorganized file system can make replicating your work difficult if not impossible. Much of the research practices discussed in the remainder of this section are aimed at supporting one or more of these three major sources of reproducibility.

## Thinking in Workflows

One way to increase the reproducibility of a project is to approach each and every task with purposeful organization and thoughtfulness. **Workflows** are the processes that we use to approach a given task. Think of checking your email. You (hopefully!) follow a series of steps when you check your email that help you organize your inbox. In his excellent primer *The workflow of data analysis using Stata* (2009), Scott Long describes a structured strategy for approaching statistical research. In Long's model, a data analysis project consists of four steps: (a) data cleaning, (b) analysis, (c) presenting results, and (d) protecting files. This is a useful model to build upon, and one that we will discuss over the course of the semester.

Even more useful, not just for statistical work but for any process, are the tasks Long lays out for each step in the data analysis workflow:

  1. Planning
  2. Organization
  3. Documentation
  4. Execution

A good example of the utility of extending this logic to other workflows is with the problem sets. The "typical" approach students take with homework assignments is to sit down, open up their software, and start with question 1. Using Long's four task approach, a workflow-based strategy to the assignment would involve beginning by reading the assignment through in its entirety to develop a **plan** for approaching it - think about what techniques and skills are needed for each step. With a plan in place, you can proceed to **organizing** yourself for the assignment - identifying and obtaining files that you will need, creating dedicated directories for saving assignment data, and getting any necessary software documentation. After pulling together all of these materials, you are ready to move on to **documentation** - setting up your assignment code and output files, and (later in the course) your research log and meta-dictionary. Once you are set-up, you would then begin to address individual assignment questions as part of the **execution** task.

The goal here is to approach everything you do for research or work with an element of mindfulness and structure about your process. This mental model for approaching research supports the creation of **reproducible** research products because we approach our work in a routinized, predictable, organized, and efficient manner. Thinking in terms of workflows also encourages a greater awareness of the complexity of tasks, which also helps you plan more accurately for how long a particular task or project will take.

In reality, there will be multiple workflows that you find yourself navigating. You will want a structured process not just for approaching a large research project like the final project, but also a process for maintaining notes related to a specific assignment, a process for documenting code, a process for approaching assignments, and even a process for backing your data up. As you go through the text, think about how to best integrate these ideas into your work habits.

## Data
One of the themes in [*Good enough practices in scientific computing*](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005510) (Wilson et al. 2017) is an emphasis on data management. One of their core messages is to ``save the raw data''. Particularly in GISc work, the raw data can be expansive - dozens of shapefiles, tabular files, and associated metadata. These files often come from disparate sources - city open data sites, the U.S. Census Bureau, state data repositories, and other federal agencies. Moreover, GIS data are often updated over time to reflect on-the-ground changes. Saving the raw data in sociospatial data science work therefore means not only creating a well-organized directory containing *all* of your original data. It also means logging the source of each file, when it was downloaded, and (if applicable) a permanent web link to your data source. For that reason, we'll give you not just the course data but a read me file and a metadictionary that lists all of the files we've disseminated to you.

A second message in the paper is to "create the data you wish to see in the world". The authors encourage readers to "create the data set you wish you had received." First and foremost, this means using open and not proprietary data formats. For spatial data, [ESRI shapefiles](https://en.wikipedia.org/wiki/Shapefile) are technically proprietary, though their standard is open. This means that other software applications, like `R` and QGIS can read and in some cases write shapefiles. For sharing spatial data, a better option is the [GeoJSON](https://en.wikipedia.org/wiki/GeoJSON), which is a plain text file format. Tabular data are best stored as `CSV` files, which is also a plain text file format that can be opened by a wide variety of applications. In contrast, common file formats like Microsoft Excel's `XLS` and `XLSX` are proprietary file packages that cannot be read as plain text and are therefore less desirable for storing data.

## Plain Text
Along with creating the data we wish to see, [*Good enough practices in scientific computing*](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005510) (Wilson et al. 2017) repeatedly emphasizes the importance of using plain text files for writing as well as for data. Using plain text file formats, like `.txt` and `.md` files, frees us from reliance on proprietary applications that we cannot be sure will exist in ten or twenty years (and are thus threats to reproducible research). They can also be opened on virtually any computer across a variety of operating systems. The authors of the article reference [Markdown] files, which a really just plain-text files containing special characters that can be rendered by websites and other applications. [Markdown], which is discussed later in this text, provides us with the best of both worlds. We can produce outputs with rich text like styling but that is saved in a plain text file container. Writing in a markup language can seem daunting at first, but within a few weeks I have found that most people can start to feel comfortable inserting markup syntax without significant cognitive burden.

## Version Control
One of the key emphases of both [*Good enough practices in scientific computing*](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005510) (Wilson et al. 2017) and ["opinionated analysis development"](https://peerj.com/preprints/3210/) is that data science work should be tracked using version control software. This text introduces [Git](https://git-scm.com) in the [Basic Git] chapter, though there are other options like [Subversion](http://subversion.apache.org) and [Mercurial](https://www.mercurial-scm.org). Git is introduced because it has been widely adopted by the `R` community and because of the robust web tools associated with [GitHub.com](http://github.com). Using version control gives us a timeline of our work along with the ability to revert back to previous versions of our files. This creates a "chain of evidence" for our research process and protects us from irrevocably altering files. 

As the authors of [*Good enough practices in scientific computing*](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005510) (Wilson et al. 2017) note, learning version control software can be tricky. There are two chapters later in this text dedicated to [Git](https://git-scm.com) covering both [Basic Git] and [Advanced Git] techniques. Those chapters also provide links to other resources and tips for using those tools successfully.