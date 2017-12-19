---
date: 2016-03-09T00:11:02+01:00
title: Package Index
weight: 42
---

The following is a list of packages used during the semester along with the lecture when they were first introduced and any subsequent lectures where they are discussed in detail. This list does not include dependencies that may be installed for these packages to work. Unless otherwise noted, packages are available via CRAN and can be installed using `base::install.packages("packageName")`.

## Base `R` Packages
- `base` - base functions ([Lecture-01](/lecture-01/))
- `stats` - statistical functions (Lecture-02)

## Data Packages
- `stlData` - St. Louis data sets (used throughout the semester)
  - install the development version via GitHub - `devtools::install_github("chrisprener/stlData")`

## Tidyverse Packages
Use `install.packages("tidyverse")` to install these for convenience!

- `dplyr` - data wrangling (Lecture-03)
- `ggplot2` - data plotting (Lecture-03)
  - install the development version via GitHub - `devtools::install_github("tidyverse/ggplot2")`
- `lubridate` - work with dates
- `stringr` - work with strings
- `tidyr` - data wrangling

## Mapping Packages
- `classInt` - data wrangling
- [`leaflet`](https://rstudio.github.io/leaflet/) - interactive maps ([Lecture-01](/lecture-01/))
- `mapproj` - map projections
- `maptools` - spatial data tools
- `RColorBrewer` - color ramps for mapping
- `rgeos` - spatial data tools
- `rgdal` - spatial data tools
- `scales` - map scales
- `sf` - spatial data tools
- `tidycensus` - census data tools

## Other Packages
- `devtools` - install packages from GitHub (Lecture-01)
- `janitor` - data wrangling and tables (Lecture-02)
- `knitr` - dynamic documents in `R` (Lecture-02)
- `RMarkdown` - markdown syntax for `R` (Lecture-02)
- `rio` - data import (Lecture-02)