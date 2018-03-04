---
date: 2016-03-09T00:11:02+01:00
title: Lecture 06 - GIS Outputs
weight: 25
---

## Meta
![](https://img.shields.io/badge/semester-spring%202018-orange.svg) ![](https://img.shields.io/badge/release-lecture-orange.svg) [![](https://img.shields.io/badge/last%20update-2018--02--26-brightgreen.svg)](https://github.com/slu-soc5650/lecture-05/blob/master/NEWS_SITE.md)

## Key Topics
[{{< tool name="ArcMap" >}}](/topic-index/#a-d)
[{{< keyword name="Cartography" >}}](/topic-index/#a-d)
[{{< package name="ggplot2" >}}](/topic-index/#q-t)
[{{< package name="ggthemes" >}}](/topic-index/#e-h)
[{{< keyword name="Map Layouts" >}}](/topic-index/#m-p)
[{{< tool name="R" >}}](/topic-index/#q-t)
[{{< package name="RColorBrewer" >}}](/topic-index/#q-t)
[{{< keyword name="Small Multiples" >}}](/topic-index/#q-t)
[{{< package name="viridis" >}}](/topic-index/#u-z)
[{{< keyword name="Wireframing" >}}](/topic-index/#u-z)

## Resources

{{< github "slu-soc5650" "lecture-06" >}}
{{< button "ArcGIS - ArcMap Processes" "https://github.com/slu-soc5650/lecture-06/blob/master/ArcMap/lecture-06-arcmap.pdf" >}}
{{< button "Functions" "https://github.com/slu-soc5650/lecture-06/blob/master/Functions/lecture-06-functions.pdf" >}}
{{< button "Lab-05" "https://github.com/slu-soc5650/lecture-06/blob/master/Lab-05/lab-05.pdf" >}}
{{< button "LP-06" "https://github.com/slu-soc5650/lecture-06/blob/master/LP-06/LP-06.pdf" >}}
{{< button "Map Handouts" "https://github.com/slu-soc5650/lecture-06/tree/master/MapHandouts" >}}
{{< button "Sample Wireframe" "https://github.com/slu-soc5650/lecture-06/tree/master/Wireframe" >}}

## Lecture Slides
<p> </p>
{{< speakerdeck 51b580eee8c34b399f67cca8862e5f5a >}}

## Lecture Prep 06 Replication
<p> </p>
{{< youtube 2iI7RszF6Go >}}

## Issues with Reading Shapefiles
A number of you reported intermittent issues with reading shapefiles into `R`. I have not been able to replicate this behavior, but wanted to offer some general advice that may help.

1. Download the entire shapefile repo from GitHub. At least some of you downloaded only the `.shp` file from GitHub and that was the source of issues. 
2. Use ArcCatalog to copy and paste shapefiles from their source into your individual project `data/` folders. Some of you reported that this addressed the issue. 
3. Use the `sf::` prefix on `st_read()`. At least one student was able to import data just fine when the following syntax was used: `sf::st_read(here("data", "dataFolder", "data.shp"), stringsAsFactors = FALSE)`
4. If nothing seems to be working, try opening the shapefile in ArcMap and see if it can be mapped. If it cannot be mapped, it is corrupt in some way and you should re-download the source data.
5. Make sure you don't have a file simultaneously open in ArcMap or ArcCatalog when you go to read it inot `R`.