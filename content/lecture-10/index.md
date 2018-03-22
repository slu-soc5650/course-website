---
date: 2016-03-09T00:11:02+01:00
title: Lecture 10 - Projections
weight: 29
---

## Meta
![](https://img.shields.io/badge/semester-spring%202018-orange.svg) 
![](https://img.shields.io/badge/release-draft-red.svg) 
[![](https://img.shields.io/badge/last%20update-2018--03--22-brightgreen.svg)](https://github.com/slu-soc5650/lecture-09/blob/master/NEWS_SITE.md)

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
{{< button "LP-09" "https://github.com/slu-soc5650/lecture-10/blob/master/assignments/lp-09/lp-09.pdf" >}}

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

