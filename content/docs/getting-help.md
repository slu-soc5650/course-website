+++
title = "Getting Help"

date = 2018-12-05T00:00:00
lastmod = 2018-12-05T00:00:00

draft = false  # Is this a draft? true/false
toc = true  # Show table of contents? true/false
type = "docs"  # Do not modify.

# Add menu entry to sidebar.
linktitle = "Getting Help"
[menu.docs]
  parent = "Fundamentals"
  weight = 4
+++

## Meta 
<i class="meta-badge semester-sp19"><i class="far fa-calendar-alt fa-lg"></i>&nbsp; **Spring 2019** </i> <i class="meta-badge progress-draft"><i class="fas fa-tasks fa-lg"></i>&nbsp; **Draft** </i> <i class="meta-badge progress-update"><i class="far fa-clock fa-lg"></i>&nbsp; **2018-12-05** </i>

## Key Topics
<a class="meta-badge tool" href="/docs/topic-index/#q-t"><i class="fas fa-desktop fa-lg"></i>&nbsp; **R**</a> <a class="meta-badge package" href="/docs/topic-index/#q-t"><i class="fas fa-archive fa-lg"></i> **reprex**</a>

## Overview
One of the biggest challenges for students first learning tools like `R`, ArcGIS, and LaTeX is dealing with the inevitable speed-bumps and errors that come along with scientific computing. Remember, first and foremost, that these tools are not consumer software. They do not always "just work", to borrow a turn of phrase from [Steve Jobs](https://en.wikipedia.org/wiki/Steve_Jobs). Learning strategies for navigating issues when the software is most definitely not working is therefore an important part of success. 

One misconception that I think is important to confront is that data analysts, software engineers, and others who appear to be experts may indeed be very good at what they do, but they are equally skilled at problem solving. This [xkcd comic](https://www.xkcd.com/627/)  illustrates (a bit sarcastically!) the point:

```{r echo=FALSE, fig.align="center", out.width = '75%'}
knitr::include_graphics("images/tech_support_cheat_sheet.png")
```

Navigating challenges with data science may not be quite as easy following the flowchart above, but there are definitely strategies for working your way through errors and challenges in data science work.

## Helping Yourself
As I noted in [Zen and the Art of Data Analysis], a key challenge of data science work is mental. One of the traits I see frequently among students who are confronted with errors is that they stop working and wait for office hours or they immediately ask a question on Slack. Both office hours and Slack are excellent options for getting help, but there are a few strategies you should pursue first. 

Before you doing anything else, however, *take a deep breath* and consider taking a break. When you being trying to fix the issue, check the time. I have spent hours trying to fix some code in `R` or mis-projected data in ArcGIS without success, and I have seen students do the same. Give yourself an hour time limit to try the steps below before you move on to constructing a reproducible example and asking for help from others. 

### Check Spelling
With `R`, the number one cause of errors that I see are misspellings. If objects in the global environment or variable names within a data frame are not spelled correctly (case matters!), you will get an error that an object cannot be found. The same goes for package and function names - they must be spelled 100% correctly.

### Check Course Resources
If the issue is one other students have come across as well, it is likely to be discussed on Slack in the relevant channel. I may have also updated some of the course handouts or the relevant lecture's course webpage with details for how to address the concern. Check both Slack and the webpage for updates before digging deeper. Check the topic index on the relevant course website ([GIS topic index](https://slu-soc5650.github.io/topic-index/)) for links to different lectures where concepts or processes were covered.

### Check Your Process
`R` functions and ArcGIS processes often have specific parameters and requirements. If you have double checked your spelling and are sure (100% sure!) that spelling is not an issue, check to make sure that you have followed all of the requirements of the workflow for the skill you are stuck on. There are two different ways to go about doing this:

- Check the course handouts and lecture slides for the relevant processes. If you cannot remember where the concepts were introduced, check the topic index on the relevant course website ([GIS topic index](https://slu-soc5650.github.io/topic-index/)). When I introduce processes, I often skip some (or many!) of the associated arguments and options, so the course materials are often easier to navigate than materials for other sources.
- Search official documentation sources:
    - For `R`, check package documentation files on CRAN. These are linked to in the package index on the relevant course website ([GIS package index](https://slu-soc5650.github.io/package-index/)). You can also use [CRAN's website](https://cran.r-project.org) to search for package information.
    - For ArcGIS, check ESRI's [official documentation files](http://desktop.arcgis.com/en/arcmap/). Make sure that you are looking at the help files for ArcGIS 10.3!
    - For Git and GitHub, check GitHub's [help website](https://help.github.com).
    - For LaTeX, [ShareLaTeX](https://www.sharelatex.com/) has an excellent set of documentation files on their [knowledge base](https://www.sharelatex.com/learn/Main_Page). [CTAN](https://ctan.org), the LaTeX package repository, also contains documentation files for all packages that can be searched.
    
Use these resources to try and narrow down what might be causing your issue. Be mindful that the root cause of an error may be several steps back in your workflow. Walk back through your process to make sure your initial steps are not the cause of the error.

### Cast a Wider Net
If none of these resources are sufficient, there are a few other options for seeking out guidance. When you search the following sites, it is often a good idea to search based on the specific error you are getting. Take out any aspects of the error that are specific to you, like a file path in ArcGIS, a file name, or a variable name. One set of options to search are the wealth of web resources that are available for some of the tools we use:

- For `R`, check out [RStudio's cheatsheets](https://www.rstudio.com/resources/cheatsheets/) and [RStudio's community forums](https://community.rstudio.com). If the package is part of the `tidyverse`, check the [website](http://tidyverse.org) as well as [R for Data Science](http://r4ds.had.co.nz). Other packages have their own websites as well. For all of these resources, links are provided in the package index on the relevant course website ([GIS package index](https://slu-soc5650.github.io/package-index/)).
- For LaTeX, there is a [LaTeX wikibook](https://en.wikibooks.org/wiki/LaTeX) with some excellent resources.
    
Another resource is [Stack Exchange](https://stackexchange.com), a network of online communities on a variety of topics including:

- [Stack Overflow](https://stackoverflow.com) for `R`, Git, and GitHub - search using tags like `[r]`, `[ggplot2]`, `[dplyr]`, `[git]`, `[github]`, etc.
- [Geographic Information Systems](https://gis.stackexchange.com) for GIS - search using the `[arcgis-desktop]` tag
- [TeX](https://tex.stackexchange.com) for LaTeX

Stack Exchange may have posts that address the issue or question you have. However, the match may only be partial and may require additional modification or tinkering to solve your specific concern. You may spend just as much time trying to get a Stack Exchange solution to work as you would waiting for a response on Slack, so proceed with caution if you decide to go this route.

Finally, if you have exhausted these other options, a Google search may be effective. This may help you identify GitHub issues, blogs, and other online tutorials that can help address whatever roadblock you have run into. Try searching first with double quotes around the main body of the error message's text. If nothing comes up, try searching without the double quotes. Search strings that include `R` package names or specific processes in ArcGIS are sometimes helpful for narrowing down a large amount of search results, especially if those results are not specific to the tool you are using. The same warning for Stack Exchange also exists for Google, however. You may find imperfect matches for your problem that take considerably more tinkering to implement. 

## How to Seek Help
If all else fails and the strategies for [Helping Yourself] have not yielded a solution, it is time to ask for help! Before you head to office hours or Slack, you will want to construct a **reproducible example**.

### What is your question?
Start with a basic step - narrow down what your question is. Neither "I am getting an error" or "This isn't working" are effective questions. What exactly is causing the error? What context does it appear in? To borrow from the examples below, a good question might be:

> I am trying to calculate descriptive statistics for an entire data frame using the `mean()` function but am getting and error. What might be the cause of the error?

> I am trying to create a thematic choropleth map in ArcGIS, but when I try and select my variable from the dropdown menu in the symbology tab under layer properties, the menu is empty. Why are all of the variables missing?

> I am trying to make my text bold in LaTeX, but the text is not rendering with bold font. I am also getting an error that says "Undefined control sequence." What is missing from my document to create bold font?

Be specific about what your issue is, and then provide a reproducible example that illustrates what you are asking about. 

### What is a reproducible example?
A reproducible example, or reprex, is a term we'll borrow from the `R` ecosystem. It was coined by [Roman François](https://twitter.com/romain_francois/status/530011023743655936) and has been enshrined in the [`reprex` package](http://reprex.tidyverse.org), which I'll describe below. The goal for a reprex is to strip down the process you have used to the minimal number of steps needed to replicate the error. This means using the fewest steps and data sources possible. Cut out anything that does not directly contribute to causing the error when making your reprex. 

I have often found that the process of making a reprex actually helps isolate the cause of the problem. For instance, it may become clear that a specific step is causing an issue. Even if you are not sure how to fix the problem, having narrowed it down can be immensely helpful. If you can use built-in data in `R` to create the reprex, or at least example data from the course, that may also help you identify whether the issue is with the process itself or something that is idiosyncratic to the data you are using. Using built-in data from `R` should be the default for any reprex you create, *unless assignment data are the cause of your issue*.

### Creating a reprex
Creating reproducible examples will differ slightly based on what you are trying to get help on.

#### `R`
To create a reprex in `R`, you will need to install the [`reprex` package](http://reprex.tidyverse.org/). It is part of the [tidyverse](https://www.tidyverse.org) but it is not installed when the `tidyverse` package is installed, so you will need to install it separately:

```r
install.packages("reprex")
```

Once you have it loaded (use the `library()` function), create a minimal example of the necessary functions that get to you to the error you are confronting. Make sure to include the `library()` functions for all packages your example depends on (except for `reprex`). Write the example in a `.R` script file (`File > New File > R Script`). For example, one might be struggling with calculating the mean of each variable in a data frame:

```r
library(ggplot2)

# assign data to data frame
data <- mpg

# attempt to calculate mean
mean(data)
```

The last of the three functions above will return this error in your `R` session:

```r
> mean(data)
[1] NA
Warning message:
In mean.default(data) : argument is not numeric or logical: returning NA
```

With the three functions written in a `.R` script, highlight all seven lines of code (the three functions, both comments, and both white space lines)  and copy them to your clipboard (`Edit > Copy`). Then call the `reprex()` function. Markdown formatted text that weaves both the functions and their output together will appear in the viewer tab:

```{r echo=FALSE, fig.align="center", out.width = '50%'}
knitr::include_graphics("images/reprex.png")
```

It will also be available on your clipboard so that you can copy and paste it into Slack or another venue that accepts Markdown syntax (like GitHub). If your reprex contains image output, such as a plot or a map, it will be automatically uploaded to imgur and a link will be embedded in your Markdown syntax. For example, say we had a question about the following code:

```r
library(ggplot2)

# assign data to data frame
data <- mpg

# plot highway mpg
ggplot(data = data, mapping = aes(x = hwy)) + 
  geom_histogram()
```

Once we copy the above code and render it using `reprex()`, it will return the following output:

``` r
library(ggplot2)

# assign data to data frame
data <- mpg

# plot highway mpg
ggplot(data = data, mapping = aes(x = hwy)) + 
  geom_histogram()
#> `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](https://i.imgur.com/8hiC7od.png)
```

The `![](hyperlink)` syntax will allow an image of your plot to appear below the code. 

The [`reprex` package website](http://reprex.tidyverse.org) has some great resources, including a [basic overview](http://reprex.tidyverse.org), some [reprex do’s and don’ts](http://reprex.tidyverse.org/articles/reprex-dos-and-donts.html), and a [detailed article](http://reprex.tidyverse.org/articles/articles/magic-reprex.html) introducing the package's functionality.

#### ArcGIS
Creating a reprex in ArcGIS is not as straightforward since there is not a dedicated tool for doing so like there is in `R`. Reprex creation is complicated by the fact that many steps you will be taking are manual. Nevertheless, it is possible to create a repex. Follow these steps:

1. In a new map document, load the minimum number of shapefiles needed to illustrate the issue you are having. Note where the shapefiles are available (in the course data release?) and what their names are.
2. Note what the coordinate system of the data frame is set to.
3. Provide notes for each step that gets you to your question or error.
4. Take a [screenshot](https://www.take-a-screenshot.org) of the error or the window you have a question about.

For example, a reprex of a question in ArcGIS could look like the following:

```
1. I have a single map shapefile open in a new map document. The shapefile is the St. Louis census tracts shapefile from the example data in the course data release.
2. The coordinate system is Missouri State Plane East (Feet)
3. When I right click on the shapefile, I click on Properties and then the Symbology tab
4. Attached is a screenshot of what the symbology tab looks like for these data.
```

#### LaTeX
Like ArcGIS, there is no specific tool for creating a reprex using LaTeX. The LaTeX community does have, however, a long tradition of creating "minimal working examples", which are similar to reprexs. Follow these general steps:

1. Create a new LaTeX project. Use the `\documentclass{article}` if you are using something different.
2. Only include packages in the preamble that are **directly** related to the question or issue you have.
3. Skip creating a title block
4. Provide just enough body text in your LaTeX document to illustrate the issue. 

A repex for LaTeX might look something like this:

```latex
\documentclass{article}

\begin{document}

\textbold{Foo bar.} Spam and eggs.

\end{document}
```

Also provide a written description of what is wrong (such as "the text is not being rendered as bold") and, if helpful, a [screenshot](https://www.take-a-screenshot.org) of your output. There is a great [overview on Stack Exchange](https://tex.meta.stackexchange.com/questions/228/ive-just-been-asked-to-write-a-minimal-example-what-is-that) of how to write a reprex for LaTeX. If you are using ShareLaTeX, also take a look at the error log and take a [screenshot](https://www.take-a-screenshot.org) of the relevant error message. If you are using another LaTeX application, provide the text of your error message instead.

#### Other Tools
For other tools we learn, such as Markdown and GitHub, you want to follow the spirit of the reprex file. Try to recreate your issue outside of the context of your assignment (this may not be possible for GitHub), and provide a detailed walk-through of the steps that you took to get where you are. For Markdown syntax, provide an example of the syntax you are using that recreates the issue or question. For GitHub, provide a [screenshot](https://www.take-a-screenshot.org) of the relevant error message.

### "I don't think I can make a reprex!"
I am 99% sure that you can! In nearly every situation I have seen students in, creating a reprex is possible. Even if the error is idiosyncratic to your computer or your data, you can absolutely clarify the context within which the error appears and minimize the amount of data, code, and other information in your `R` code or your map document. For the less than 1% of scenarios where a reprex is not possible, the process of writing a question, clarifying the context and steps you took to get there, and producing an example of the error will still make it easier for me to help you. 

### "Isn't this a lot of work?"
Well, yes, it does require some extra effort. This effort is almost always worth it, however. In some cases, the time it takes you to produce the repex leads you to the answer on your own, which is part of the problem solving process that this class is designed to foster. Even when this does not happen, making reprex informed inquires is a technique that you will be able to take with you at the end of the semester. Even if you are not working in a technical setting, being able to structure clear, concise questions about a process is a valuable skill! 

Finally, creating a reprex saves you time in the long run. When I get vague questions, it often takes some experimenting on my part to reproduce the error. If you send me a question with a reproducible error, you cut out that experimentation time on my end and I can get right to answering your question. Likewise, students often come to office hours without an example of their issue ready to go and hope that I can conjure in my mind the scenario they are describing. Despite my best efforts, I am usually unable to do so and ask students to reproduce the error during office hours. If you come to office hours with a reprex, we can get to answering your question right away!

## Where to Seek Help
Once you have tried [Helping Yourself] and have gone through the steps outlined in [How to Seek Help] (i.e. made a reprex), it is time to ask your question. There are a number of different places that you can pose questions. The sections below outline these and suggest some ways to make your question most effective.

### Internal Venues
Within the confines of the course, the two best places to ask questions are on Slack and during office hours. When asking a question on Slack, please consider doing so in a public channel. This helps others learn from the question that you have. The only course-related questions that are not appropriate for Slack are those that reference specific parts of a problem set or the final project. However, if you are creating reproducible examples, your questions should not be that specific even if they ultimately are about a homework assignment. If you are not sure whether the question is appropriate or not for a public channel, or just would prefer not to ask your question out in the open, feel free to send me a [direct message on Slack](https://get.slack.help/hc/en-us/articles/212281468-Direct-messages-and-group-DMs).

When you pose a question on Slack, it should contain three or four pieces of information:

1. The question itself - what are you hoping to get help with?
2. A reproducible example - give as many details as you need to clearly illustrate the question
3. A [screenshot](https://www.take-a-screenshot.org) or image output that illustrates your reprex
4. What you've tried - lay out the steps you took to quickly ("I've checked the spelling, gone through the Lecture 03 documents, looked at the `dplyr` website, and have done a quick Google search.")

Post your reprex as a [snippet](https://get.slack.help/hc/en-us/articles/204145658-Create-a-snippet) in Slack by:

1. Clicking the plus sign on the left side of the message box
2. Selecting **Code or text snippet**
3. Filling out the pop-up window

If you are posting a reprex from `R`, remove the three backticks and the letter `r` from the first line as well as the three backticks from the bottom line. If you are including an image hyperlink created by the `reprex` package, remove that from the code snippet and paste it into Slack separately. A good question on Slack should look like this:

```{r echo=FALSE, fig.align="center", out.width = '90%'}
knitr::include_graphics("images/slackQuestion.png")
```

This same general process holds for asking questions in person - come ready with a solid question, a reproducible example, and be ready to pull it up on your computer or a lab computer.

### External Venues
There are two good places to ask questions external to the course as well. For questions related to RStudio, R Markdown, and the [tidyverse](http://tidyverse.org), RStudio maintains a web forum called [RStudio Community](https://community.rstudio.com). If you are posting there, you can use `reprex()` to generate Markdown formatted reprexs.

Another place to post questions in on one of the relevant [Stack Exchange](https://stackexchange.com) communities:

- [Stack Overflow](https://stackoverflow.com) for `R`, Git, and GitHub - post using tags like `[r]`, `[ggplot2]`, `[dplyr]`, `[git]`, `[github]`, etc.
- [Geographic Information Systems](https://gis.stackexchange.com) for GIS - post using the `[arcgis-desktop]` tag
- [TeX](https://tex.stackexchange.com) for LaTeX

Before you post, search thoroughly to make sure that your question has not already been answered. Stack Exchange has strong norms about how to post appropriately. You can descriptions of what makes a good post [here](https://codereview.stackexchange.com/help/how-to-ask) and [here](https://stackoverflow.com/help/how-to-ask). You can also find a description of [what not to ask](https://stackoverflow.com/help/dont-ask). If you are going to post on Stack Overflow, the `reprex()` function can be modified to produce well-formatted output specific to that site by adding the `venue` argument, as in `reprex(venue = "so")`.

Of the two sites, I find [RStudio Community](https://community.rstudio.com) to be a friendlier place that is more relaxed than Stack Overflow and its cousins. However, Stack Exchange communities have much larger user bases to draw from.