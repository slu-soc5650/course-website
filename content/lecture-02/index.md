---
date: 2016-03-09T00:11:02+01:00
title: Lecture 02 - Working with Data (Part 1)
weight: 21
---
![](https://img.shields.io/badge/semester-spring%202018-orange.svg) ![](https://img.shields.io/badge/release-lecture-orange.svg) [![](https://img.shields.io/badge/last%20update-2018--01--29-brightgreen.svg)](https://github.com/slu-soc5650/lecture-02/blob/master/NEWS_SITE.md)

## Key Topics
[{{< keyword name="Analysis development" >}}](/topic-index/#a-d)
[{{< package name="ggplot2" >}}](/topic-index/#e-h)
[{{< package name="here" >}}](/topic-index/#e-h)
[{{< package name="knitr" >}}](/topic-index/#i-l)
[{{< tool name="R" >}}](/topic-index/#q-t)
[{{< keyword name="R projects" >}}](/topic-index/#q-t)
[{{< package name="reprex" >}}](/topic-index/#q-t)
[{{< keyword name="Reproducible Examples" >}}](/topic-index/#a-d)
[{{< package name="rmarkdown" >}}](/topic-index/#q-t)
[{{< package name="stlData" >}}](/topic-index/#q-t)

## Resources

{{< github "slu-soc5650" "lecture-02" >}}
{{< button "Exercise - Analysis" "https://github.com/slu-soc5650/lecture-02/blob/master/Exercises/exercise-02a-Analysis.pdf" >}}
{{< button "Exercise - Plotting" "https://github.com/slu-soc5650/lecture-02/blob/master/Exercises/exercise-02b-Plotting.pdf" >}}
{{< button "Functions" "https://github.com/slu-soc5650/lecture-02/blob/master/Functions/lecture-02-functions.pdf" >}}
{{< button "LP-02" "https://github.com/slu-soc5650/lecture-02/blob/master/LP-02/LP-02.pdf" >}}
{{< button "Workflow - Projects" "https://github.com/slu-soc5650/lecture-02/blob/master/Workflows/workflow-02a-projects.pdf" >}}
{{< button "Workflow - Reprex" "https://github.com/slu-soc5650/lecture-02/blob/master/Workflows/workflow-02b-reprex.pdf" >}}

## Lecture Slides
{{< speakerdeck 2bdbdb0699fb4f248f6e6308ed92a065 >}}

## Lecture Prep 02 Replication

{{< youtube 2eYE679k7rs >}}

You should also check out the `.Rmd` replication file in the [`lecture-02` repository](https://github.com/slu-soc5650/lecture-02/tree/master/LP-02).

## Costs of Open Data
The first topic covered tonight was the pros and cons of open data. Here are a few links to material that were referenced in the lecture. These roughly follow the order in which they were introduced:

* [U.S. Project Open Data](https://project-open-data.cio.gov)
* "It's getting hot in here: Looking at heat-related 311 reports in Boston homes" - [Katie Jollie](http://katiejolly.io/blog/2018-01-22/heat-reports-boston)
* "Spies in the Skies" - [BuzzFeed](https://www.buzzfeed.com/peteraldhous/spies-in-the-skies)
* [City of St. Louis Open Data Portal](https://www.stlouis-mo.gov/data/)
* [St. Louis County Open Data Portal](http://data-stlcogis.opendata.arcgis.com)
* [City of Cambridge Open GIS](https://github.com/cambridgegis)
* [County of Los Angeles Open Data Portal](https://data.lacounty.gov)
* [Socrata](https://socrata.com)
* "How much do 'open data' portals cost So Cal governments?" - [Southern California Public Radio](https://www.scpr.org/news/2015/06/24/52343/how-much-do-open-data-portals-cost-so-cal-governme/)
* "The (Hidden) Cost of Open Data" - [governing.com](http://www.governing.com/columns/tech-talk/gov-open-data-cost-problems.html)
* "U.S. soldiers are revealing sensitive and dangerous information by jogging" - [Washington Post](https://www.washingtonpost.com/world/a-map-showing-the-users-of-fitness-devices-lets-the-world-see-where-us-soldiers-are-and-what-they-are-doing/2018/01/28/86915662-0441-11e8-aa61-f3391373867e_story.html)
* [Strava Heat Map](https://labs.strava.com/heatmap)

If you'd like to read a bit more on this topic, I suggest this article from *Transactions in GIS*, a fantastic peer reviewed journal:

* Johnson, Peter A., et al. 2017. "The Cost (s) of Geospatial Open Data." *Transactions in GIS* 21(3):434-445. \[[Full Text](http://onlinelibrary.wiley.com/doi/10.1111/tgis.12283)\]

## Project Organization
One of the topics covered this week is an extension of a [reading from last week](https://chris-prener.github.io/SSDSBook/protecting-your-work.html) - how to organize projects. I've posted a sample project complete with a R Notebook, `html` output, and `github_document` output. You can check out the project [here](https://github.com/chris-prener/sampleNotebook).

