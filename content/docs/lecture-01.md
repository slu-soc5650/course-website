+++
title = "Lecture-01 - Course Introduction"

date = 2018-12-05T00:00:00
lastmod = 2018-12-05T00:00:00

draft = false  # Is this a draft? true/false
toc = true  # Show table of contents? true/false
type = "docs"  # Do not modify.

# Add menu entry to sidebar.
linktitle = "Lecture-01 - Introduction"
[menu.docs]
  parent = "Lectures"
  weight = 3
+++

## Meta
<i class="meta-badge semester-sp19"><i class="far fa-calendar-alt fa-lg"></i>&nbsp; **Spring 2019** </i> <i class="meta-badge progress-lecture"><i class="fas fa-tasks fa-lg"></i>&nbsp; **Lecture** </i> <i class="meta-badge progress-update"><i class="far fa-clock fa-lg"></i>&nbsp; **2018-12-05** </i>

## Key Topics
<a class="meta-badge keyword" href="/docs/topic-index/#a-d"><i class="fas fa-tags fa-lg"></i>&nbsp; **Analysis development**</a> <a class="meta-badge package" href="/docs/topic-index/#a-d"><i class="fas fa-archive fa-lg"></i> **base**</a> <a class="meta-badge keyword" href="/docs/topic-index/#a-d"><i class="fas fa-tags fa-lg"></i>&nbsp; **Cartography**</a> <a class="meta-badge keyword" href="/docs/topic-index/#i-l"><i class="fas fa-tags fa-lg"></i>&nbsp; **Interactive maps**</a> <a class="meta-badge package" href="/docs/topic-index/#i-l"><i class="fas fa-archive fa-lg"></i> **leaflet**</a>

## Resources
<a class="btn btn-outline-primary resource" href="https://github.com/slu-soc5650/lecture-01/blob/master/handouts/lecture-01-email.pdf" target="_blank"> Exercise - Email </a> <a class="btn btn-outline-primary resource" href="https://github.com/slu-soc5650/lecture-01/blob/master/handouts/lecture-01-shawCrime.pdf" target="_blank"> Exercise - Shaw Crime </a> <a class="btn btn-outline-primary resource" href="https://github.com/slu-soc5650/lecture-01/blob/master/handouts/lecture-01-functions.pdf" target="_blank"> Functions </a>

## Lecture Slides
<p> </p>
<script async class="speakerdeck-embed" data-id="3b023eb9d7ee463faea3a90532221987" data-ratio="1.33333333333333" src="//speakerdeck.com/assets/embed.js"></script>
<p> </p>

## Working with R Packages
During the semester, we'll use some sample data for in-class exercises and lecture examples. To make things easy, these data available as an `R` package called [`stlData`](https://chris-prener.github.io/stlData/). Packages are small software programs that extend `R`'s base functionality. Most packages we'll use this semester are available via [CRAN](https://cran.r-project.org). To get started, you'll need to fire up RStudio. In the console, enter the following function and hit return:

```r
install.packages("stldata")
```

Once it installs, we can access the data included in `stldata` by loading the package:

```r
library("stlData")
```

This will be our standard workflow for installing packages this semester.

## Leaflet Basics
As a way to get to know `R` and RStudio, we'll be working with the `R` package [`leaflet`](https://rstudio.github.io/leaflet/). `leaflet` is the `R` implementation of [`leaflet.js`](http://leafletjs.com), an open-source Java Script library for building interactive maps. To get started, you'll need to install `leaflet` via CRAN:

```r
install.packages("leaflet")
```

Just like before, we can open `leaflet` with the `library()` function:

```r
library("leaflet")
```

### A Simple Map

`leaflet` itself is straightforward to get up and running. If we wanted an interactive map with a marker placed on-top of Morrissey Hall, we would use the following script entered into `R`:

```r
leaflet() %>%
  addTiles() %>%
  addMarkers(lng=-90.237104, lat=38.637547, popup="Morrissey Hall")
```

The `leaflet()` function creates a map widget, and the `addTiles()` function adds a basemap to it. By default, [OpenStreetMap](https://www.openstreetmap.org) is used for the basemap. Finally, we use `addMarkers()` to specify the longitude and latitude of our marker, and we enter in a label that will appear as a pop-up when a user clicks on the marker. `lng`, `lat`, and `popup` are all called "arguments" - these are used to control how a function operates. 

The `%>%` is called the "pipe operator", and it is used to chain together functions in what we will call "pipelines". This pipeline can be read like a list, with the word **then** substituted for each instance of `%>%`:

1. First we create a map widget, **then**
2. we add basemap tiles, **then**
3. we add a marker at the given longitude and latitude.

The code chunk above produces the following map in RStudio's **Viewer** tab:

![leaflet01](/images/leaflet01.png)

You can use the **Show in new window** icon (a white box with a small arrow facing up and right) to open the map in your web browser.

### Changing the Basemap

To alter the basemap, we can use `addProviderTiles()` in place of `addTiles()`. I like the CartoDB "Positron" basemap. To use the Positron basemap, we create a second pipeline:

```r
leaflet() %>%
  addProviderTiles(providers$CartoDB.Positron) %>% 
  addMarkers(lng=-90.237104, lat=38.637547, popup="Morrissey Hall")
```

Two things are important to note here. When we load the `leaflet` package, we have access to a data object called `providers`. You can use `names(providers)` to explore it. `providers` is a vector of items, each of which corresponds to a different basemap. We can select one of those items, `CartoDB.Positron`, by separating `providers` from the item name with a dollar sign (`$`). This is a classic way in which elements of a data set are accessed in `R` syntax.

The second code chunk produces the following map in RStudio's **Viewer** tab:

![leaflet02](/images/leaflet02.png)

## Loading and Exploring Data
Our example data package, [`stlData`](https://chris-prener.github.io/stlData/), contains a simple table of some places that I frequent around campus in addition to Morrissey Hall. In the package, it is called `sluPlaces`. We can reference these data in our `leaflet()` call and again in the `addMarkers()` function to project (map) them onto our basemap. First, we need to assign these data to an object in our global environment. We'll take the `sluPlaces` table and assign it to the object `sluData`:

```r
sluData <- sluPlaces
```

Notice how we always assign data in reverse like this, and that we don't use an equal sign. [These are both just R quirks that take some getting used to](http://blog.revolutionanalytics.com/2008/12/use-equals-or-arrow-for-assignment.html). We can explore the data a number of ways, including with the `View()` function and the `str()` function:

```r
> View(sluData)

> str(sluData)
'data.frame':	6 obs. of  4 variables:
 $ id  : num  1 2 3 4 5 6
 $ name: chr  "Morrissey Hall" "Starbucks" "Simon Rec" "Pius Library" ...
 $ lng : num  -90.2 -90.2 -90.2 -90.2 -90.2 ...
 $ lat : num  38.6 38.6 38.6 38.6 38.6 ...
```

The `View()` function does not produce any console output, but does open a viewer that (reassuringly for some of you!) looks a bit like a spreadsheet. The `str()` function gives us an overview of the structure of an object - typically the variables included in the data along with some sample values.

## Data Sources and Leaflet
Now that we have some data loaded in our global environment, we can project (map) it using `leaflet`. We need to reference the data frame (our data object) in the `leaflet()` call and both the longitude (`lng`) and latitude (`lat`) variable names in our `addMarkers()` call. We'll also set the `name` variable to be the source for the popup text:

```r
leaflet(data = sluData) %>%
  addProviderTiles(providers$CartoDB.Positron) %>%  # Add alternative map tiles
  addMarkers(lng = ~lng, lat = ~lat, popup = ~name)
```

Notice how we use the tilde symbol (`~`) in `addMarkers()` before the variable names. This is idiosyncratic to `leaflet`. 

The code chunk produces the following plot:

![leaflet03](/images/leaflet03.png)

Congratulations - you have now made three maps!

## Replication Code
All of the code used in our lecture today, in one place:
