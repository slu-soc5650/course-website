---
date: 2016-03-09T00:11:02+01:00
title: Lecture 09 - Spatial Joins
weight: 28
---

## Meta
![](https://img.shields.io/badge/semester-spring%202018-orange.svg) 
![](https://img.shields.io/badge/release-full-brightgreen.svg) 
[![](https://img.shields.io/badge/last%20update-2018--03--22-brightgreen.svg)](https://github.com/slu-soc5650/lecture-09/blob/master/NEWS_SITE.md)

## Key Topics
[{{< tool name="ArcMap" >}}](/topic-index/#a-d)
[{{< package name="dplyr" >}}](/topic-index/#q-t)
[{{< tool name="R" >}}](/topic-index/#q-t)
[{{< keyword name="Spatial Joins" >}}](/topic-index/#q-t)
[{{< keyword name="Table Joins" >}}](/topic-index/#q-t)
[{{< keyword name="Writing Data" >}}](/topic-index/#u-z)

## Resources

{{< github "slu-soc5650" "lecture-09" >}}
{{< button "ArcMap Processes" "https://github.com/slu-soc5650/lecture-09/blob/master/handouts/lecture-09-arcmap.pdf" >}}
{{< button "Functions" "https://github.com/slu-soc5650/lecture-09/blob/master/handouts/lecture-09-functions.pdf" >}}
{{< button "Lab-06" "https://github.com/slu-soc5650/lecture-09/blob/master/assignments/lab-08/lab-08.pdf" >}}
{{< button "LP-08" "https://github.com/slu-soc5650/lecture-09/blob/master/assignments/lp-08/lp-08.pdf" >}}
{{< button "PS-05" "https://github.com/slu-soc5650/lecture-09/blob/master/assignments/ps-05/ps-05.pdf" >}}

## Lecture Slides
<p> </p>
{{< speakerdeck 0060e503b40448448bfdc73cb336b4e7 >}}

## Lecture Prep 08 Replication
<p> </p>
{{< youtube yqm0mirGzFY >}}

## Whacky Variable Names
The data for PS-05 included a variable name with a space in it, which presents unique challenges for recoding data. The best course of action is to rename the variable to one that is more appropriately named. There are two ways to do this. One way is to use the `rename()` from `dplyr`:

```r
x <- rename(x, estimated_value = `estimated value`)
```

Notice how the backtick symbol was used on each end of the multi-word variable name to encompass it in its entirety. This will work in `R` functions any time there is a multi-word variable. 

The other way to deal with this is to use `clean_names()` to adjust the variable name automatically:

```
> clean_names(x)
  id estimated_value
1  1              22
2  2              44
```

There are no special arguments needed to get `clean_names()` to work with these data - it will handle multi-word variable names just fine.

