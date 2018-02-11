---
date: 2016-03-09T00:11:02+01:00
title: Lecture 03 - The Nature of Spatial Data (Part 1)
weight: 22
---
![](https://img.shields.io/badge/semester-spring%202018-orange.svg) ![](https://img.shields.io/badge/release-updated-brightgreen.svg) [![](https://img.shields.io/badge/last%20update-2018--02--06-brightgreen.svg)](https://github.com/slu-soc5650/lecture-03/blob/master/NEWS_SITE.md)

## Key Topics
[{{< package name="dplyr" >}}](/topic-index/#q-t)
[{{< keyword name="Data structures" >}}](/topic-index/#a-d)
[{{< keyword name="Data wrangling" >}}](/topic-index/#a-d)
[{{< package name="here" >}}](/topic-index/#e-h)
[{{< keyword name="GIS and policy support" >}}](/topic-index/#e-h)
[{{< package name="janitor" >}}](/topic-index/#i-l)
[{{< package name="naniar" >}}](/topic-index/#m-p)
[{{< keyword name="Normalization" >}}](/topic-index/#m-p)
[{{< keyword name="Open data" >}}](/topic-index/#m-p)
[{{< tool name="R" >}}](/topic-index/#q-t)
[{{< keyword name="R projects" >}}](/topic-index/#q-t)
[{{< package name="readr" >}}](/topic-index/#q-t)
[{{< package name="reprex" >}}](/topic-index/#q-t)
[{{< keyword name="Representation" >}}](/topic-index/#q-t)
[{{< keyword name="Reproducible Examples" >}}](/topic-index/#q-t)
[{{< keyword name="Scale" >}}](/topic-index/#q-t)
[{{< keyword name="Spatial autocorrelation" >}}](/topic-index/#q-t)

## Resources

{{< github "slu-soc5650" "lecture-03" >}}
{{< button "Functions" "https://github.com/slu-soc5650/lecture-03/blob/master/Functions/lecture-03-functions.pdf" >}}
{{< button "LP-03" "https://github.com/slu-soc5650/lecture-02/blob/master/LP-02/LP-03.pdf" >}}

## Lecture Slides
<p> </p>
{{< speakerdeck 2bdbdb0699fb4f248f6e6308ed92a065 >}}

## Lecture Prep 02 Replication
<p> </p>
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

We also walked through the Git and GitHub workflow we'll be using this semester. I've replicated that exercise as a YouTube video for folks who want some additional examples of how to use Git, GitHub, and GitHub Desktop together.

<p> </p>
{{< youtube zU1YghiEIoY >}}

## Some Initial Thoughts on `R`
In working on our first notebooks and bits of code, a number of themes have emerged. One of the central ones has to do with the accuracy required with typing. Unlike Microsoft Word, `R` expects a very high degree of precision in what is type. Something as simple as forgetting a closing parenthesis `)` or a missing double quote `"` can trigger an error. These lessons remind me of a section from [Kieran Healy's](https://kieranhealy.org) new book [Data Visualization: A practical introduction](http://socviz.co):

> Like all programming languages, R does exactly what you tell it to, rather than exactly what you want it to. This can make it frustrating to work with. It is as if one had an endlessly energetic, powerful, but also extremely literal-minded robot to order around. Remember that no-one writes fluent, error-free code on the first go all the time. From simple typos to big misunderstandings, mistakes are a standard part of the activity of programming. This is why error-checking, debugging, and testing are also a central part of programming. So, just try to be patient with yourself and with R while you use it. Expect to make errors, and don’t worry when that happens. You won’t break anything. Each time you figure out why a bit of code has gone wrong you will have learned a new thing about how the language works.

As I said in class, be mindful both of the need for precision and for the commonality of experiencing a variety of errors at this stage in your learning process. Make sure you build time in for errors to come up as you plan your workweeks!