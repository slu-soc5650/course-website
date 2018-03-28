---
date: 2016-03-09T00:11:02+01:00
title: Lecture 10 - Projections
weight: 29
---

## Meta
![](https://img.shields.io/badge/semester-spring%202018-orange.svg) 
![](https://img.shields.io/badge/release-updated-brightgreen.svg) 
[![](https://img.shields.io/badge/last%20update-2018--03--28-brightgreen.svg)](https://github.com/slu-soc5650/lecture-09/blob/master/NEWS_SITE.md)

## Key Topics
[{{< tool name="ArcMap" >}}](/topic-index/#a-d)
[{{< keyword name="Geographic coordinate systems" >}}](/topic-index/#e-h)
[{{< tool name="R" >}}](/topic-index/#q-t)
[{{< package name="sf" >}}](/topic-index/#q-t)
[{{< keyword name="Projected coordinate systems" >}}](/topic-index/#m-p)
[{{< keyword name="Projecting data" >}}](/topic-index/#m-p)

## Resources

{{< github "slu-soc5650" "lecture-10" >}}
{{< button "ArcMap Processes" "https://github.com/slu-soc5650/lecture-10/blob/master/handouts/lecture-10-arcmap.pdf" >}}
{{< button "Functions" "https://github.com/slu-soc5650/lecture-10/blob/master/handouts/lecture-10-functions.pdf" >}}
{{< button "Lab-09" "https://github.com/slu-soc5650/lecture-10/blob/master/assignments/lab-09/lab-09.pdf" >}}
{{< button "LP-09" "https://github.com/slu-soc5650/lecture-10/blob/master/assignments/lp-09/lp-09.pdf" >}}
{{< button "PS-06" "https://github.com/slu-soc5650/lecture-10/blob/master/assignments/ps-06/ps-06.pdf" >}}

## Lecture Slides
<p> </p>
{{< speakerdeck b5ad8a7638cd441c8e1d4f95dc169454 >}}

## Lecture Prep 09 Replication
<p> </p>
{{< youtube emYUhqQxoOs >}}

## Videos From Lecture
### Scene from *The West Wing*, Season 2, Episode 16 - "The Gall-Peters Projection"
<p> </p>
{{< youtube vVX-PrBRtTY >}}

### Vox.com - "Why all world maps are wrong"
<p> </p>
{{< youtube kIID5FDi2JQ >}}

## The True Size
The interactive mapping tool described during the lecture - "The True Size" - can be found [here](https://thetruesize.com).

## Missouri Projection Systems
The website [Spatial Reference](http://www.spatialreference.org/) has a [comprehensive list](http://www.spatialreference.org/ref/?search=Missouri) of projections used for mapping Missouri. The `EPSG` values can be used as inputs in `sf` functions whenever a `crs` value is needed.

## Table Joins with County Data
Beware that county-level tables for the entire United States are exceptionally large, and the `left_join()` function becomes correspondingly slow. One way to improve the performance of this process is to drop as many variables as you possibly can from each table. The key items to retain for both the lab and the problem set are columns like name, state FIPS, county, fips, and geoid data as well as the relevant county-level outcome (health insurance, stroke rates, etc).

Dropping variables also gets us around an issue with the `ALAND10` and `AWATER10` variables. Both of these variables contain very large numbers - the square meters of water and land respectively for each county. ESRI's shapefile standards to not allow us to store these data as numbers - they have to be stored as string instead:

```r
countyData %>%
  mutate(ALAND10 = as.character(ALAND10)) %>%
  mutate(AWATER10 = as.character(AWATER10)) -> countyData
```

This leaves us with two character or string vectors instead of numeric ones, which will not cause errors with the ESRI shapefile standard. If you do not complete this transformation for both variables, you will get errors when you go to write the data to shapefile at the end of your notebook.

## Including leaftlet in Notebooks
When we include `leaflet` in RNotebooks, we need to adjust our `YAML` header before we knit the notebook. Here is the header from the lab replication file:

```YAML
---
title: "Lab 09 Replication Notebook"
author: "Christopher Prener, Ph.D."
date: '(`r format(Sys.time(), "%B %d, %Y")`)'
output: 
  github_document: default
  html_notebook: default 
always_allow_html: yes
---
```

The `always_allow_html: yes` line at the end of the `YAML` allows you to knit the notebook without getting an error. If you get any `knitr` errors while trying to finish the notebook, check to make sure you've added this text to the header!

Beware that the `leaflet` objects won't actually appear in your notebook - the code should appear but with no output. This is the expected behavior with `leaflet`!


