---
date: 2016-03-09T00:11:02+01:00
title: Course Preview
weight: 15
---

To set the stage for this semester, please watch the two videos below. These will take approximately 35 minutes to view. Once you have finished these videos, follow the link at the bottom of the page to answer a few short questions about what you saw.

## Key Topics
{{< keyword name="Analysis development" >}}
{{< keyword name="Interactive maps" >}}
{{< keyword name="Open data" >}}
{{< keyword name="Reproducibility" >}}

## Open Data and GIS in Los Angeles
One of the course learning outcomes is titled "GISc and Public Policy". Much of the data that we will use this semseter is available to us because governmental agencies at the Federal, state, and local levels have published it and made it accessible. We call the movement to make as much data available as possible "open data". 

Different governments have embraced the open data movement to varying degrees, and the video below discusses Los Angeles' integration of open data and GIS. It is a 9 minute talk given by L.A.'s former Chief Data Officer [Lilian P. Coral](https://twitter.com/lcoral). The talk was part of a conference organized by [ESRI](https://www.esri.com/en-us/home), the makers of ArcGIS.

</br>
{{< youtube etdwa768Zms >}}
</br>

Once you've watched the video, check out the web application featured in the video that [visualizes pedestrian and cyclist injuries in Los Angeles](http://ladot.maps.arcgis.com/apps/MapJournal/index.html?appid=a45d3efd7b1d4ef49f362caadb4754b0). You can also visit L.A.'s open data website called [GeoHub](http://geohub.lacity.org).

## Analysis Development
Making a produce like L.A.'s visualization of pedestrian and cyclist injuries is a complicated effort. Data must be obtained from various sources, modified (a process we call "data wrangling" or "data clearning"), and then linked with map coordinates. Once it is ready to be mapped, the web application must be designed and created. We'll call this large-scale process a "workflow" this semester. 

The workflow that we'll use is opinionated - there is a strong premise that underlies the workflow about the ways in which spatial data (and data more generally) should be obtained, stored, modified, and mapped. Hilary Parker is a data scientist at [Stichfix](http://stitchfix.com) and also runs a data science podcast called [Not So Standard Deviations](http://nssdeviations.com). She has been speaking recently about an idea called opionated analysis development. The [video](https://www.rstudio.com/resources/videos/opinionated-analysis-development/) linked to below is a 25 minute talk she gave on this idea last year, and she now has a [draft paper](https://peerj.com/preprints/3210/) out on the topic as well. Our workflow for this semester is closely linked to the ideas she discusses in this talk.

</br>
[![opinionatedAnalysis](/images/opinionatedAnalysis.png)](https://www.rstudio.com/resources/videos/opinionated-analysis-development/)
</br>

Many (but not all of you) will have experienced some parts of these processes before. Perhaps you've used Microsoft Excel to organize some information or used SPSS to analyze some quantitative data. We won't be using those tools. Instead, this course will emphasize the use of other tools that support reproducibile, accurate, and collaborative data analysis. Thoughout the semester, we'll discuss why these tools are important and the advantages they have over other products that are out there. Inspired by Hilary's idea of opinionated analysis development, our goal each week will be to focus on the *processes* that can be used to increase the reproducibility and accuracy of our geospatial work.

## Lecture Prep 01
The lecture prep for the first week asks three follow-up questions about these videos and L.A.'s interactive website. Please answer these questions and submit them before class on **January 22nd**. Answers **must** be submitted through [Google Forms](https://goo.gl/forms/vgHqTPagXyrsrk4I3) and each response should be three to four sentances in length. The questions are provided here for reference:

1. Briefly describe how the City of Los Angeles uses data and mapping to inform how they deliver city services.
2. After viewing the interactive map showing pedestrian and cyclist injuries, describe what you thought of the map. Some example considerations could include: was it easy to read? to navigate? did you like the colors? was it missing relevant data?
3. In your own words, what are the key aspects of opinionated analysis development?
