---
date: 2016-03-09T00:11:02+01:00
title: Lecture 03 - The Nature of Spatial Data (Part 1)
weight: 22
---

## Meta
![](https://img.shields.io/badge/semester-spring%202018-orange.svg) ![](https://img.shields.io/badge/release-updated-brightgreen.svg) [![](https://img.shields.io/badge/last%20update-2018--02--12-brightgreen.svg)](https://github.com/slu-soc5650/lecture-03/blob/master/NEWS_SITE.md)

## Key Topics
[{{< package name="dplyr" >}}](/topic-index/#q-t)
[{{< keyword name="Data types" >}}](/topic-index/#a-d)
[{{< keyword name="Data wrangling" >}}](/topic-index/#a-d)
[{{< package name="here" >}}](/topic-index/#e-h)
[{{< keyword name="GIS and policy support" >}}](/topic-index/#e-h)
[{{< package name="janitor" >}}](/topic-index/#i-l)
[{{< keyword name="Levels of measurement" >}}](/topic-index/#i-l)
[{{< package name="magrittr" >}}](/topic-index/#m-p)
[{{< package name="naniar" >}}](/topic-index/#m-p)
[{{< keyword name="Normalization" >}}](/topic-index/#m-p)
[{{< tool name="R" >}}](/topic-index/#q-t)
[{{< package name="readr" >}}](/topic-index/#q-t)
[{{< package name="reprex" >}}](/topic-index/#q-t)
[{{< keyword name="Representation" >}}](/topic-index/#q-t)
[{{< keyword name="Reproducible Examples" >}}](/topic-index/#q-t)
[{{< keyword name="Scale" >}}](/topic-index/#q-t)
[{{< keyword name="Spatial autocorrelation" >}}](/topic-index/#q-t)

## Resources

{{< github "slu-soc5650" "lecture-03" >}}
{{< button "Functions" "https://github.com/slu-soc5650/lecture-03/blob/master/Functions/lecture-03-functions.pdf" >}}
{{< button "Lab-02" "https://github.com/slu-soc5650/lecture-03/tree/master/Lab-02">}}
{{< button "LP-03" "https://github.com/slu-soc5650/lecture-03/blob/master/LP-03/LP-03.pdf" >}}
{{< button "PS-01" "https://github.com/slu-soc5650/lecture-03/tree/master/PS-01">}}
{{< button "Workflow - Data Wrangling" "https://github.com/slu-soc5650/lecture-03/blob/master/Workflows/workflow-03-wrangling.pdf">}}


## Lecture Slides
<p> </p>
{{< speakerdeck 8e734fd11e354f88ae88fb2c15d61c1d >}}

## Lecture Prep 03 Replication
<p> </p>
{{< youtube qxHNWpHLxUA >}}

You should also check out the `.Rmd` replication file in the [`lecture-03` repository](https://github.com/slu-soc5650/lecture-03/blob/master/LP-03).

## reprex
### Implementing Reproducible Examples
We've been working on creating reproducible examples for the past two weeks. Remember that the goal of reproducible examples is to create short, clear examples of a bug or an error that you are getting or to illustrate a particular concept. Here are a couple things to remember as you go through the [`reprex` workflow](https://github.com/slu-soc5650/lecture-02/blob/master/Workflows/workflow-02-reprex.pdf):

1. Make sure you load *only* the packages needed for your example. This will likely be different from the list of packages needed for a particular assignment. If there is a package you use in your assignment that does not impact the code for the repex, don't include it!
2. Use sample data (i.e. `mpg` from `ggplot2`, `starwars` from `dplyr`, or any of the data from `stlData`). This accomplishes a number things:
  * You are selecting data that is accessible to the audience you are communicating with and does not require any external setup or files. This makes it *easier* to reproduce the phenomenon you're describing.
  * You are forced to *generalize* your issue, parsing out what is idiosyncratic to your data from what is a more general question or concern about how a particular function or group of functions work.
  * The process of *abstracting* your issue from the specifics of your code may help you answer your question by helping you identify how the code *should* work (if your reprex executes without error).
3. Make sure you are making the small edits to the output when you paste it into Slack - this will help the reprex appear as cleanly as possible. These edits are described in the [`reprex` workflow handout](https://github.com/slu-soc5650/lecture-02/blob/master/Workflows/workflow-02-reprex.pdf).

### Errors with reprex
This week, two errors with the `reprex` package seemed to be widespread. The first involved an error message that the clipboard was unavailable:

```r
> library(reprex)
> # copy code to clipboard
> reprex()
No input provided and clipboard is not available.
```

This error surfaced on any computer running `reprex` version 1.2, which is the current version of CRAN (as of 2/12/18). In early January, it seems that CRAN maintainers went through packages that had access to the clipboard and disabled that functionality without notifying maintainers. In the case of `reprex`, the package was also declared "orphaned" (meaning no longer maintained). 

The second error is present on any computer running `reprex` in conjunction with an older version of [`pandoc`](https://pandoc.org). `pandoc` is the magic behind knitr - it can convert text files between different formats with ease (i.e. from Markdown to HTML every time you save your notebook). On SLU's lab computers, which have an older version of `pandoc`, this second error was also popping up:

```r
> library(reprex)
> # copy code to clipboard
> reprex()
Rendering reprex...
pandoc.exe: unrecognized option `--quiet'
Try pandoc.exe --help for more information.
Error: pandoc document conversion failed with error 2
```

I [reported this bug](https://github.com/tidyverse/reprex/issues/178) to the developers and they patched `reprex` so that it will work with older versions of `pandoc`. The first error, involving the clipboard, has also been patched. However neither of these patches are available on CRAN. For right now, please install the [development version](https://github.com/tidyverse/reprex) of `reprex` from GitHub:

```r
devtools::install_github("tidyverse/reprex")
```

## janitor
### Anticipating Changes
One issue that is cropping up this week are conflicts in folks' code between `clean_names()` and `rename()`. This seems to be happening largely in the code chunk where variables are being renamed. Here is a reprex:

```r
library(dplyr)
library(janitor)
library(stlData)

str(stlAsthma)
#> 'data.frame':    106 obs. of  6 variables:
#>  $ geoID         : num  2.95e+10 2.95e+10 2.95e+10 2.95e+10 2.95e+10 ...
#>  $ tractCE       : int  118100 117400 126700 119102 126800 126900 108100 127000 127400 103700 ...
#>  $ nameLSAD      : Factor w/ 106 levels "Census Tract 1011",..: 76 75 97 80 98 99 36 100 104 15 ...
#>  $ pctAsthma     : num  11.9 9.6 14.5 9 9.3 13.6 12.7 12.8 12.7 8.6 ...
#>  $ pctAsthma_Low : num  11.1 9.3 13.5 8.5 8.8 12.6 11.8 11.7 11.9 8.1 ...
#>  $ pctAsthma_High: num  12.7 10 15.5 9.7 9.8 14.6 13.8 14.2 13.8 9.2 ...

stlAsthma %>%
  clean_names(case = "snake") %>%
  rename(low_estimate = pctAsthma_Low) -> asthma
#> Error: `pctAsthma_Low` contains unknown variables
```

The `clean_names()` function renames `pctAsthma_low` to `pct_asthma_low`. However, when I wrote the above reprex, I did not anticipate this change and instead wrote the `rename()` function using the original variable name. Writing pipelines requires some presence of mind - you need to imagine how the data changes from line to line and write subsequent lines of code accordingly. 

I find it helpful to write pipelines one line at a time:

```r
# first iteration
stlAsthma %>%
  clean_names(case = "snake") -> asthma

# second iteration
stlAsthma %>%
  clean_names(case = "snake") %>%
  rename(low_estimate = pct_asthma_low) -> asthma
```

The code block above shows two iterations of the same pipeline. I run it one, check the output, and then add a second line based on the output of the first. This iterative process ensures that I am writing the `rename()` function based not on my *assumption* of how `clean_names()` impacts the data but rather based on me actually visualizing that change. 

### Errors with janitor
Another error that was widespread this week, at least for Windows users, was one where `clean_names()` from the `janitor` package only worked in a particular context:

```r
> library(janitor)
> library(stlData)
> murders <- clean_names(stlMurders, case = "snake")
# Error in clean_names(., case.names = "snake") : unused argument (case.names = "snake")
```

This error persisted when other styles of variable naming were selected (like camel case). This is a known bug with the current CRAN release (version 0.3.1) that has been patched in the [development version on GitHub](https://github.com/sfirke/janitor). For now, install `janitor` from GitHub instead of from CRAN:

```r
devtools::install_github("sfirke/janitor")
```

## here
Next up in our list of package surprises, we had some intermittent issues with reading csv data into `R`. Like the `janitor` error, these were limited to Windows users. The error manifests itself when you go to either read or write data from an R notebook:

```r
> riverData <- read_csv("data/rawData.csv")
Error: 'rawData.csv' does not exist in current working directory ('F:/SOC5650/DoeAssignments/Labs/Lab-99/docs')
```

I also suspect (but have not demonstrated) that the `ggplot2` errors folks received with the lecture-02 assignments are also related to this error. 

After experimenting with two students' notebooks (on the `read_csv()` error) and [reporting this as a bug on GitHub](https://github.com/krlmlr/here/issues/14), I have both a workaround and a more stable fix for this error.

### The Cause
The cause of this error is that `here::here()` has not been tested with the specific combination of functions we are using in the project setup code chunk:

```r
knitr::opts_knit$set(root.dir = here::here())
```

At least for some Windows machines some of the time, this code chunk is being evaluated but, for some unknown reason, the working directory identified by `here()` is not being set as the root directory by `knitr`. This means that, when your notebook should be loading data out of the `data/` subfolder or saving output to the `results/` subfolder, it is looking *inside* the `docs/` subfolder instead of correctly identifying both `data/` and `results/` as subdirectories of the project directory.

### Workaround
The quick workaround is to manually execute the project setup code chunk if you get an error, and then re-run all of the code chunks in your notebook. Executing it manually seems to give `knitr` the chance to correctly set its root directory whereas it cannot if you run all of the code chunks at once. *If you are working interactively with your notebook, you need to make sure you do this anyway.*

### Stable Fix
The more stable fix is to jettison the project setup code chunk from your notebook entirely and follow [the advice](https://github.com/krlmlr/here/issues/14#issuecomment-364692725) from the `here` package's developer. This involves using here when you load or save data. 

The `here()` function takes as arguments the quoted name of a subfolder followed by the quoted name of the file. These should be separated by a comma:

```r
here("data", "rawData.csv")
```

When you use it this way, you need to embed this function wherever you would normally enter a manual file path of some kind:

```r
read_csv(here("data", "rawData.csv"))
```

Here is an example of this use of `here()` in context:

```r
> library(here)
> library(readr)
> data <- read_csv(here("data", "rawData.csv"))
```

In the example above, `here()` converts the input into a relative path that looks like `data/rawData.csv`. This same syntax can work with multiple layers of folders and subfolders:

```r
> library(here)
> library(readr)
> data <- read_csv(here("data", "tabularData", "rawData.csv"))
```

In the example above, `here()` converts the input into a relative path that looks like `data/tabularData/rawData.csv`. We can use the same logic to save output:

```r
> library(here)
> library(ggplot2)
> ggplot() + geom_histogram(mpg, mapping = aes(hwy))
> ggsave(here("results", "histogram.png"))
```

### Why This is Worth It
It is more remembering why this is worth it. Using `here()` makes your projects portable. You can move the directory on your own computer, or give it to a colleague (or your professor!) and the code will always execute (assuming they have the correct packages installed). This is because you never specify manual location where your working directory (i.e. the folder with your `.Rproj` file) is located. This is a *huge* plus for reproducibility.
