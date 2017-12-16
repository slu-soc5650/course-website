---
date: 2016-03-09T00:11:02+01:00
title: Package Index
weight: 42
---

The following is a list of packages used during the semester along with the lecture when they were first introduced and any subsequent lectures where they are discussed in detail. This list does not include dependencies that may be installed for these packages to work. Unless otherwise noted, packages are available via CRAN and can be installed using `base::install.packages("packageName")`.

## Base `R`
- `base` - base functions (Lecture-01)
- `stats` - statistical functions

## Data
- `stlData` - St. Louis data sets (Lecture-02)
  - install the development version via GitHub - `devtools::install_github("chrisprener/stlData")`

## Tidyverse
Use `install.packages("tidyverse")` to install these for convenience!

- `dplyr` - data wrangling (Lecture-02)
- `ggplot2` - data plotting (Lecture-02)
  - install the development version via GitHub - `devtools::install_github("tidyverse/ggplot2")`
- `lubridate` - work with dates
- `readr` - data import (Lecture-02)
- `stringr` - work with strings
- `tidyr` - data wrangling

## Mapping Packages
- `classInt` - data wrangling
- `mapproj` - map projections
- `maptools` - spatial data tools
- `RColorBrewer` - color ramps for mapping
- `rgeos` - spatial data tools
- `rgdal` - spatial data tools
- `scales` - map scales
- `sf` - spatial data tools
- `tidycensus` - census data tools

## Other Packages
- `devtools` - install packages from GitHub (Lecture-02)
- `janitor` - data wrangling and tables (Lecture-02)
- `knitr` - dynamic documents in `R` (Lecture-01)
- `RMarkdown` - markdown syntax for `R` (Lecture-01)