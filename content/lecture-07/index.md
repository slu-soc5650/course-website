---
date: 2016-03-09T00:11:02+01:00
title: Lecture 07 - Geodatabases
weight: 25
---

## Meta
![](https://img.shields.io/badge/semester-spring%202018-orange.svg) ![](https://img.shields.io/badge/release-draft-red.svg) [![](https://img.shields.io/badge/last%20update-2018--03--04-brightgreen.svg)](https://github.com/slu-soc5650/lecture-07/blob/master/NEWS_SITE.md)

## Key Topics
[{{< tool name="ArcCatalog" >}}](/topic-index/#a-d)
[{{< keyword name="Geodatabases" >}}](/topic-index/#e-h)
[{{< tool name="R" >}}](/topic-index/#q-t)
[{{< package name="readr" >}}](/topic-index/#q-t)
[{{< package name="sf" >}}](/topic-index/#q-t)
[{{< keyword name="Writing Data" >}}](/topic-index/#u-z)

## Resources

{{< github "slu-soc5650" "lecture-07" >}}
{{< button "LP-07" "https://github.com/slu-soc5650/lecture-07/blob/master/LP-07/LP-07.pdf" >}}

## Re-writing Shapefiles in R
Some of you may have been confronted with an error in the lecture prep when you went to knitr your notebook after testing all of its code:

![](/images/knitrSfError.png)

By default, the `st_write()` function will not overwrite an existing shapefile. You can alter this behavior by re-structuring the function to add the `delete_dsn` option:

```r
st_write(here("data", "dataFolder", "data.shp"), delete_dsn = TRUE)
```

If you do this from the start, however, you will also get an error that the file does not exist. This error isn't a true error in the sense that the shapefile still gets written. So, my advice would be to keep `delete_dsn = TRUE` and remind yourself that you will get an "error" the first time you execute the code. After that, however, you should not get additional errors.