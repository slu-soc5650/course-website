---
date: 2016-03-09T00:11:02+01:00
title: Lecture 07 - Geodatabases
weight: 26
---

## Meta
![](https://img.shields.io/badge/semester-spring%202018-orange.svg) ![](https://img.shields.io/badge/release-updated-brightgreen.svg) [![](https://img.shields.io/badge/last%20update-2018--03--30-brightgreen.svg)](https://github.com/slu-soc5650/lecture-07/blob/master/NEWS_SITE.md)

## Key Topics
[{{< tool name="ArcCatalog" >}}](/topic-index/#a-d)
[{{< keyword name="Data wrangling" >}}](/topic-index/#a-d)
[{{< keyword name="Geodatabases" >}}](/topic-index/#e-h)
[{{< package name="lubridate" >}}](/topic-index/#q-t)
[{{< tool name="R" >}}](/topic-index/#q-t)
[{{< package name="readr" >}}](/topic-index/#q-t)
[{{< package name="sf" >}}](/topic-index/#q-t)
[{{< package name="stringr" >}}](/topic-index/#q-t)
[{{< keyword name="Writing Data" >}}](/topic-index/#u-z)

## Resources

{{< github "slu-soc5650" "lecture-07" >}}
{{< button "Functions" "https://github.com/slu-soc5650/lecture-07/blob/master/Functions/lecture-07-functions.pdf" >}}
{{< button "Lab-06" "https://github.com/slu-soc5650/lecture-07/blob/master/Lab-06/lab-06.pdf" >}}
{{< button "LP-07" "https://github.com/slu-soc5650/lecture-07/blob/master/LP-07/LP-07.pdf" >}}

## Lecture Slides
<p> </p>
{{< speakerdeck ff6667777234406d8d79eb70633a28cf >}}

## Re-writing Shapefiles in R
Some of you may have been confronted with an error in the lecture prep when you went to knitr your notebook after testing all of its code:

![](/images/knitrSfError.png)

By default, the `st_write()` function will not overwrite an existing shapefile. You can alter this behavior by re-structuring the function to add the `delete_dsn` option:

```r
st_write(here("data", "dataFolder", "data.shp"), delete_dsn = TRUE)
```

If you do this from the start, however, you will also get an error that the file does not exist. This error isn't a true error in the sense that the shapefile still gets written. So, my advice would be to keep `delete_dsn = TRUE` and remind yourself that you will get an "error" the first time you execute the code. After that, however, you should not get additional errors.

## Conflicts with lubridate and here
We have run into an error with `lubridate` and `here` that manifests itself with the following message:

```r
> x <- read_csv(here("data", "rawData.csv"))
Error in here("data", "rawData.csv") : 
  unused arguments ("data", "rawData.csv")
```

If you find yourself getting an error message like this that involves "unused arguments", the source of the error is likely to be a conflict with the `lubridate` package. `R` users get used to ignoring the warnings and notes that appear after loading packages using `library()`. However, the key to addressing this error is in those warnings. When we load `here` first and then `lubriate`, this is what the output looks like:

```r
> library(here)
here() starts at /Users/chris/GitHub/SOC5650/test
>
> library(lubridate)

Attaching package: ‘lubridate’

The following object is masked from ‘package:here’:

    here

The following object is masked from ‘package:base’:

    date
```

The key is in the note that the object `here` is `masked from ‘package:here’`. This is an indication that the `here()` function from the `here` package is no longer accessible in your `R` session. When two packages have identically named functions - `lubridate` also has a function called `here()` - the package loaded last gets precedence over a package or packages loaded earlier in the `R` session. 

One way to work around this is to call both the package name and the function name together: 

```r
here::here()
```

This is cumbersome, however, and I recommend loading `lubridate` *before* `here` in your dependencies code chunk to mitigate this conflict:

```r
# tidyverse packages
library(dplyr)
library(ggplot2)
library(lubridate)

# other packages
library(here)
```

This will prevent `lubridate` from stepping on the `here` package's toes.