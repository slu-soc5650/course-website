+++
title = "Lecture-01 - Course Introduction"

date = 2018-12-05T00:00:00
lastmod = 2020-01-17T00:00:00

draft = false  # Is this a draft? true/false
toc = true  # Show table of contents? true/false
type = "docs"  # Do not modify.

# Add menu entry to sidebar.
linktitle = "Lecture-01 - Introduction"
[menu.docs]
  parent = "Lectures"
  weight = 3

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 5
+++

## Resources
<a class="btn btn-outline-primary resource" href="https://slu-soc5650.github.io/syllabus/lecture-01-course-introduction.html" target="_blank"><i class="fas fa-book fa-lg"></i>&nbsp; View on Syllabus </a> 
<a class="btn btn-outline-primary resource" href="https://github.com/slu-soc5650/lecture-01" target="_blank"><i class="fab fa-github fa-lg"></i>&nbsp; View on GitHub </a> 
<a class="btn btn-outline-primary resource" href="https://github.com/slu-soc5650/lecture-01/blob/master/handouts/lecture-01-email.pdf" target="_blank"><i class="fas fa-file-pdf fa-lg"></i>&nbsp; Exercise - Email </a> 
<a class="btn btn-outline-primary resource" href="https://github.com/slu-soc5650/lecture-01/blob/master/handouts/lecture-01-functions.pdf" target="_blank"><i class="fas fa-file-pdf fa-lg"></i>&nbsp; Functions </a>

## Lecture Slides
<p> </p>
<script async class="speakerdeck-embed" data-id="3b023eb9d7ee463faea3a90532221987" data-ratio="1.33333333333333" src="//speakerdeck.com/assets/embed.js"></script>
<p> </p>

## Leaflet Basics
As a way to get to know `R` and RStudio, we'll be working with the `R` package [`leaflet`](https://rstudio.github.io/leaflet/). `leaflet` is the `R` implementation of [`leaflet.js`](http://leafletjs.com), an open-source Java Script library for building interactive maps. To get started, you'll need to install `leaflet` and a number of other packages via CRAN:

```r
install.packages(c("here", "leaflet", "sf", "tidyverse", "usethis"))
```

We can open `leaflet` and the other packages we'll need with the `library()` function:

```r
library("here")
library("leaflet")
library("magrittr")
library("readr")
library("sf")
```

### Get Data
To get data quickly for today, you can use the following code snippet in your console:

```r
usethis::use_course("https://github.com/slu-soc5650/lecture-01/archive/master.zip")
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

![leaflet01](/images/lecture-01/map1.png)

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

![leaflet02](/images/lecture-01/map2.png)

### Adding Additional Points

The `data/sluPlaces.csv` file (a `.csv` file is a type of spreadsheet) contains information on a couple of other places where I find myself regularly on campus. We can read it into `R` using the `readr` package (part of the tidyverse):

```r
sluPlaces <- read_csv(here("data", "sluPlaces.csv"))
```

We read the statement from right to left - the data found at `data/sluPlaces.csv` is read correctly as `.csv` data, and the resulting imported data is stored in an object in our global environment named `sluPlaces`. The `here()` function helps us write simple, operating system agnostic file paths that will always be relative to where the `.Rproj` file is stored. We'll talk more about this as the semester progresses.

We can explore the data a number of ways, including with the `View()` (output not shown) function and the `str()` function:

```r
str(sluPlaces)
```

If we wanted to use `View()`, it would be implemented like this:

```r
View(sluPlaces)
```

When executed in the console, it will produce a spreadsheet-like view within RStudio.

The `.csv` data are *tabular* data - they contain longitude and latitude data, but they are not *projected*. This means we are missing the geometric data that locates these longitude and latitude data in space. leaflet can take these spatial references, however, and convert them to usable geometric data. We do so using a very similar process to what we did before:

```r
leaflet(data = sluPlaces) %>%
  addProviderTiles(providers$CartoDB.Positron) %>% 
  addMarkers(lng = ~lng, lat = ~lat, popup = ~name)
```

The `data = sluPlaces` argument in `leaflet()` directs `R` to the appropriate data set to map. We use the tilde (`~`) to indicate to leaflet that these are variables within `sluPlaces`.

The code chunk produces the following plot:

![leaflet03](/images/lecture-01/map3.png)

### Reading in Spatial Data

For data that have already been converted to geometric data, we use the `sf` package to read them. The importing process looks similar to what we used with the `.csv` file. We'll demonstrate this with the violent crime data for Shaw:

```r
shawViolent <- st_read(here("data", "SHAW_Violent_2018.shp"), stringsAsFactors = FALSE)
```

We'll still use `here()` to specify the file path, but the function is different now because we need a specialized tool for geometric data. Note that we open the `.shp` file - this is the primary piece of the *family* of files that together contain all of the relevant information to locate the Shaw violent crime data in space and describe it. We work with `SHAW_Violent_2018.shp`, but the other parts must be present as well.

To map these data, we no longer need to specify `lng` and `lat` because we're using geometric data as well:

```r
leaflet(data = shawViolent) %>%
  addProviderTiles(providers$CartoDB.Positron) %>% 
  addMarkers(popup = ~crimeCt)
```

We use the simplified crime category (`crimeCt`) for the popup this time.

The code chunk produces the following plot:

![leaflet04](/images/lecture-01/map4.png)

Finally, we can make a similar map with all Part 1 crimes:

```r
shawP1 <- st_read(here("data", "SHAW_Part1_2018.shp"), stringsAsFactors = FALSE)
```

And then we'll map them:

```r
leaflet(data = shawP1) %>%
  addProviderTiles(providers$CartoDB.Positron) %>% 
  addMarkers(popup = ~crimeCt)
```

![leaflet05](/images/lecture-01/map5.png)
