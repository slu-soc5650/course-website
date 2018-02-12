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

I also suspect (but have not demonstrated) that the `ggplot2` errors folks recived with the lecture-02 assignments are also related to this error. 

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
> library(here)
here() starts at F:/SOC5650/DoeAssignments/Labs/Lab-99
> library(readr)
> data <- read_csv("data", "rawData.csv")
Parsed with column specification:
cols(
  .default = col_character(),
  year = col_integer(),
  name = col_character()
)
See spec(...) for full column specifications.
```

In the example above, `here()` converts the input into a relative path that looks like `data/rawData.csv`. This same syntax can work with multiple layers of folders and subfolders:

```r
> library(here)
here() starts at F:/SOC5650/DoeAssignments/Labs/Lab-99
> library(readr)
> data <- read_csv("data", "tabularData", "rawData.csv")Parsed with column specification:
cols(
  .default = col_character(),
  year = col_integer(),
  name = col_character()
)
See spec(...) for full column specifications.
```

In the example above, `here()` converts the input into a relative path that looks like `data/tabularData/rawData.csv`. We can use the same logic to save output:

```r
> library(here)
here() starts at F:/SOC5650/DoeAssignments/Labs/Lab-99
> library(ggplot2)
> ggplot() + geom_histogram(mpg, mapping = aes(hwy))
> ggsave("results", "histogram.png")
Saving 7.04 x 6.86 in image
`stat_bin()` using `bins = 30`. Pick better value with `binwidth`.
```

