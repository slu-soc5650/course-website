---
date: 2016-03-09T00:11:02+01:00
title: Lecture 04 - The Nature of Spatial Data (Part 2)
weight: 23
---

## Meta
![](https://img.shields.io/badge/semester-spring%202018-orange.svg) ![](https://img.shields.io/badge/release-lecture-orange.svg) [![](https://img.shields.io/badge/last%20update-2018--02--12-brightgreen.svg)](https://github.com/slu-soc5650/lecture-04/blob/master/NEWS_SITE.md)

## Key Topics
[{{< keyword name="Analysis development" >}}](/topic-index/#a-d)
[{{< tool name="ArcCatalog" >}}](/topic-index/#a-d)
[{{< tool name="ArcMap" >}}](/topic-index/#a-d)
[{{< keyword name="Cartography" >}}](/topic-index/#a-d)
[{{< keyword name="Census geography" >}}](/topic-index/#q-t)
[{{< keyword name="Coordinate systems" >}}](/topic-index/#a-d)
[{{< keyword name="Decision making in GIS" >}}](/topic-index/#a-d)
[{{< keyword name="Geodatabases" >}}](/topic-index/#e-h)
[{{< package name="ggplot2" >}}](/topic-index/#q-t)
[{{< tool name="R" >}}](/topic-index/#q-t)
[{{< keyword name="Representation" >}}](/topic-index/#q-t)
[{{< keyword name="Representing place" >}}](/topic-index/#q-t)
[{{< keyword name="Scale" >}}](/topic-index/#q-t)
[{{< package name="sf" >}}](/topic-index/#q-t)
[{{< keyword name="Shapefiles" >}}](/topic-index/#q-t)

## Resources

{{< github "slu-soc5650" "lecture-04" >}}
{{< button "ArcGIS - ArcCatalog Processes" "https://github.com/slu-soc5650/lecture-04/blob/master/ArcGIS/lecture-04-arccatalog.pdf" >}}
{{< button "ArcGIS - ArcMap Processes" "https://github.com/slu-soc5650/lecture-04/blob/master/ArcGIS/lecture-04-arcmap.pdf" >}}
{{< button "Functions" "https://github.com/slu-soc5650/lecture-04/blob/master/Functions/lecture-04-functions.pdf" >}}
{{< button "Lab-03" "https://github.com/slu-soc5650/lecture-04/blob/master/Lab-03/lab-03.pdf" >}}
{{< button "LP-04" "https://github.com/slu-soc5650/lecture-04/blob/master/LP-04/LP-04.pdf" >}}

## Lecture Slides
<p> </p>
{{< speakerdeck aa6c2a6508d44d8c94b47e3efb024e09 >}}

## Lecture Prep 04 Replication
<p> </p>
{{< youtube OlgUSP_5bLM >}}

## sf
`sf` is a package for working with spatial data in `R`. It is the most "modern", which means it can sometimes be difficult to find examples or help online. This has changed significantly since I first started using it, and the developers are continuing to add vignettes and expand their userbase. To install `sf`:

```r
install.packages("sf")
```

### Installation on Windows
To install `sf` on Windows, you need to have [RTools](https://cran.r-project.org/bin/windows/Rtools/) installed. RTools is a suite of tools for building packages on Windows, and it will allow sf to install a number of spatial data libraries that it requires to read and process shapefiles. These tools require administrative rights, so you may have to enter your password and on lab computers you will be taken to an alternate screen where you'll have to agree to a special set of terms of use from the University.

### Installation on macOS
Users on macOS will have to install the spatial data libraries on their own. An omnibus installer is available from the [Kyng Chaos website](https://www.kyngchaos.com/software/frameworks) - you'll want to download and run the GDAL 2.2 Complete installer. 

## ggplot2
To use `sf` for map making, we'll need the *development* version of `ggplot2`. The current CRAN release *does not* have the `geom_sf()` function, but the *development* version on GitHub does. 

### Installation
Before you install it, you'll need to install a package called `rlang`:

```r
install.packages("rlang")
```

You'll never need to load `rlang` for this class but it needs to be available on your system. Once that is installed, you can install `ggplot2` using `devtools`:

```r
devtools::install_github("ggplot2")
```

Some Windows users reported errors in class last night where the dependency `digest` did not install. If you get that error, please install it manually:

```r
install.packages("digest")
```

### Data Sources with geom_sf()

There are two bugs to be aware of with `geom_sf()`. One is the need to explicitly declare the data argument in the `geom`:

```r
> library(ggplot2)
> library(stlData)
> ggplot() +
+     geom_sf(stlBoundary, fill = "#5d5d5d", color = "#5d5d5d")
Error: `mapping` must be created by `aes()`
```

Not declaring the data source will result in errors like theone above. You can address this by explicitly declaring the `data` argument:

```r
library(ggplot2)
library(stlData)
ggplot() +
  geom_sf(data = stlBoundary, fill = "#5d5d5d", color = "#5d5d5d")
```

### Polygon Edge Not Found
When using `geom_sf()` with multiple layers, the following error message seems to pop up regularly. When I tested it this past weekend, it was erroring every second or third time I ran the following reprex:

```r
> library(ggplot2)
> library(stlData)
> ggplot() +
+   geom_sf(data = stlBoundary, fill = "#5d5d5d", color = "#5d5d5d") +
+   geom_sf(data = stlHistoric, fill = "#d48a72", color = "#d48a72") +
+   geom_sf(data = stlHydro, fill = "#72bcd4", color = "#72bcd4")
Error in grid.Call(C_textBounds, as.graphicsAnnot(x$label), x$x, x$y,  : 
  polygon edge not found
```

The good news is that executing it repetedly did produce plots without error each time, so if you get the error re-execute the code once or twice and you should get a plot!
