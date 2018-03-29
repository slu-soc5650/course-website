---
date: 2016-03-09T00:11:02+01:00
title: Final Project
weight: 40
---
![](https://img.shields.io/badge/semester-spring%202018-orange.svg) ![](https://img.shields.io/badge/release-full-brightgreen.svg) ![](https://img.shields.io/badge/last%20update-2017--03--29-brightgreen.svg)

## Core Files

{{< github "slu-soc5650" "finalProject" >}}
{{< button "Data" "https://github.com/slu-soc5650/finalProject/tree/master/rawData" >}}
{{< button "Directions" "https://github.com/slu-soc5650/finalProject/blob/master/finalProject.pdf" >}}
{{< button "Groups" "https://github.com/slu-soc5650/finalProject/blob/master/groups2018.md" >}}

## Overview

The final project for this course requires students to clean and map non-emergency call data from the City of St. Louis. These data describe the presence of various types of problems in City neighborhoods. The project brings together many of the scientific computing and GI science skills that are developed over the course of the semester. It also models the collaborative nature of GI science work by asking students to complete some aspects of the final project as a group using the collaborative development (GitHub) and communication (Slack) tools we have learned this semester. This guide contains instructions for completing the final project.

## Waypoints

The final project instructions include "waypoints" - designated check-in times for students to ensure that everyone continues to make consistent forward progress throughout the semester (see the [**Syllabus**](https://github.com/slu-soc5650/Core-Documents/blob/master/syllabus.pdf) and the [**Directions**](https://github.com/slu-soc5650/finalProject/blob/master/finalProject.pdf)). The next waypoint will be highlighted with **bold** font throughout the semester.

1. Lecture-03 (February 5) - Topic memo submitted as a GitHub issue in each student's assignment repository
2. Lecture-05 (February 19) - Meeting report posted in each group's Slack channel
3. Lecture-07 (March 5) - Progress report from each student due in group's Slack channel
4. **Lecture-11 (April 2) - Draft materials due in each student's assignment repository**
5. Lecture-13 (April 16) - Response to reviewer due as a GitHub issue in each student's assignment repository
6. Lecture-15 (April 30) - Progress report from each student due as a GitHub issue in each student's assignment repository

## Data Cleaning
### Importing Data on Windows Computers
We've identified a difference in the way that `.csv` data are imported by Windows computers that has implications for how the `srx` and `sry` variables are read in. Please use the following syntax to "force" `readr` to import that `srx` and `sry` variables as `double` rather than `integer` values:

```r
csb <- read_csv(here("data", "csbCreate.csv"),
                col_types = cols(
                  srx = col_double(),
                  sry = col_double()
                ))
```

This should help ensure that you reach the desired sample size.

### Filtering Based on Number of Characters
To accomplish this step, use the `nchar()` function from the `base` package. `nchar()` returns the number of characters in a string. For example, we could filter some hypothetical data with a variable named `x` based on whether or not `x` had 3 or more characters:

```r
data <- filter(data, nchar(x) >= 3)
```

Remember that, with `filter()`, you want to identify the observations you wish to *keep*.

## Clarifications
The newly released updates to the final project instructions have made the following clarifications:

1. Pages 7 and 8 - expectations for the draft materials have been clarified
2. Page 8 - a paragraph titled "Who Does What?" was added to clarify some questions about the distinction between group and individual workloads.
3. Page 37 - the due date has been clarified as a **suggested** due date. 
4. Page 38 - the final cleaned sample size of the full data set should be $n=721444$.
5. Page 39 - the process has been clarified so that data are projected using `R` and not ArcGIS.
6. Page 41 - the due date has been clarified as a **suggested** due date. 
7. Pages 42 and 43 - clarify demographic download and cleaning instructions - all work should be done in `R` and not ArcGIS.
8. Vignette 4 - clarify pagnation
9. Page 46 - clarify that the pre-existing folders in the repo should be used for storing shapefiles
10. Page 50 - add alternate source for city point data since the Iowa website no longer exists
11. Page 55 - the due date has been clarified as a **suggested** due date. 
12. Page 55 and 56 - clarify that the pre-existing folders in the repo should be used for storing geodatabases
13. Page 63 - the due date has been clarified as a **suggested** due date. 
14. Page 64 - clarify that the pre-existing folders in the repo should be used for storing map files
