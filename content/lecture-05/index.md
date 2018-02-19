---
date: 2016-03-09T00:11:02+01:00
title: Lecture 05 - Cartographic Design
weight: 24
---

## Meta
![](https://img.shields.io/badge/semester-spring%202018-orange.svg) ![](https://img.shields.io/badge/release-full-brightgreen.svg) [![](https://img.shields.io/badge/last%20update-2018--02--15-brightgreen.svg)](https://github.com/slu-soc5650/lecture-05/blob/master/NEWS_SITE.md)

## Key Topics
[{{< tool name="ArcMap" >}}](/topic-index/#a-d)
[{{< package name="dplyr" >}}](/topic-index/#q-t)
[{{< keyword name="Cartography" >}}](/topic-index/#a-d)
[{{< package name="ggplot2" >}}](/topic-index/#q-t)
[{{< tool name="R" >}}](/topic-index/#q-t)
[{{< package name="RColorBrewer" >}}](/topic-index/#q-t)
[{{< package name="sf" >}}](/topic-index/#q-t)
[{{< package name="viridis" >}}](/topic-index/#u-z)

## Resources

{{< github "slu-soc5650" "lecture-05" >}}
{{< button "ArcGIS - ArcMap Processes" "https://github.com/slu-soc5650/lecture-05/blob/master/ArcMap/lecture-05-arcmap.pdf" >}}
{{< button "Functions" "https://github.com/slu-soc5650/lecture-05/blob/master/Functions/lecture-05-functions.pdf" >}}
{{< button "Lab-03" "https://github.com/slu-soc5650/lecture-05/blob/master/Lab-04/lab-04.pdf" >}}
{{< button "LP-05" "https://github.com/slu-soc5650/lecture-05/blob/master/LP-05/LP-05.pdf" >}}
{{< button "PS-03" "https://github.com/slu-soc5650/lecture-05/blob/master/PS-03/ps-03.pdf" >}}

## Lecture Slides
<p> </p>
{{< speakerdeck f0a0dbfca2994777bc019e75e8cbeb12 >}}

## Lecture Prep 05 Replication
<p> </p>
{{< youtube IT9d_27bkN0 >}}

## Updates to `stlData`
The `stlData` package has been updated! You can check out how it has changed by reading through its [`README`](https://github.com/chris-prener/stlData). The one potential impact is that, if you have older code that refers to the `stlLead` data set, you will need to update it to refer to `stl_tbl_lead`. To update the package, use the same process you used to initiall install it:

```r
devtools::install_github("chris-prener/stlData")
```

We'll begin referring to the updated version in class this week!

## Data for Lab-04
There is an additional set of data needed for Lab-04 that is not available in the course data release. You can download it from [GitHub](https://github.com/slu-openGIS/MO_DEMOS_JeffCityRegion) by using the large green "Clone or download" button. Either cloning or downloading the `.zip` file works for this assignment.

## ArcGIS Color Styles
Color style files are available for both the Color Brewer set of palettes and what we'll call the "viridis" palette set. Viridis is actually the default set of color ramps for [matplotlib](https://en.wikipedia.org/wiki/Matplotlib), the Python plotting library. ArcGIS uses `.style` files to provide additional symbology options for users. Both the `ColorBrewer.style` and the `matplotlib.style` files are available on GitHub. I have "forked" both repositories so that they can be easily found within our course organization. Forking is a way to creating a personal copy of another user's repository that contains links back to the original so that it can be updated if necessary. Forks reflect their parent repository's name by default, so you can find our forks of these two repositories in the following places:

* [`slu-soc5650/GISTaskSheets`](https://github.com/slu-soc5650/GISTaskSheets) for `ColorBrewer.style`
* [`slu-soc5650/matplotlib-arcgis`](https://github.com/slu-soc5650/matplotlib-arcgis) for `matplotlib.style`

Both relevant style files are available in the top-level of these repos. You will not need their contents otherwise. Steps for installing these files are available on [this week's ArcMap processes handout](https://github.com/slu-soc5650/lecture-05/blob/master/ArcMap/lecture-05-arcmap.pdf).

## `colorblindr`
This week I've made reference to the `colorblindr` package, which you can access from [GitHub](https://github.com/clauswilke/colorblindr). Installation does not always go smoothly, and it will not work with plots objects if they are created in the console (it is still in active development), but it is a very cool tool once you get the hang of it. Using it for class is **not required**.