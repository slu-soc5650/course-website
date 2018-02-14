---
date: 2016-03-09T00:11:02+01:00
title: Package Index
weight: 42
---
![](https://img.shields.io/badge/semester-spring%202018-orange.svg) ![](https://img.shields.io/badge/release-updated-brightgreen.svg) ![](https://img.shields.io/badge/last%20update-2018--02--13-brightgreen.svg)

The following is a list of packages used during the semester along with links to additional resources. This list does not include dependencies that may be installed for these packages to work. Unless otherwise noted, packages are available via CRAN and can be installed using `base::install.packages("packageName")`.

### Icon reference

- <i class="pgkIndex"><i class="fas fa-list"></i></i> - Topic index
- <i class="pkgResource"><i class="fas fa-database"></i></i> - CRAN site
- <i class="pkgResource"><i class="fab fa-github"></i></i> - GitHub repo
- <i class="pkgResource"><i class="fas fa-home"></i></i> - Website
- <i class="pkgResource"><i class="fas fa-file"></i></i> - RStudio Cheatsheet
- <i class="pkgResource"><i class="fas fa-book"></i></i> - Book

## Base `R` Packages
- `base` - base functions {{< pkgIndex "#q-t" >}} {{< pkgWeb "https://stat.ethz.ch/R-manual/R-patched/library/base/html/00Index.html" >}}
- `stats` - statistical functions {{< pkgIndex "#q-t" >}} {{< pkgWeb "https://stat.ethz.ch/R-manual/R-patched/library/stats/html/00Index.html"  >}}
- `utils` - utility functions {{< pkgIndex "#u-z" >}} {{< pkgWeb "https://stat.ethz.ch/R-manual/R-patched/library/utils/html/00Index.html" >}}

## Data Packages
- `stlData` - St. Louis data sets {{< pkgIndex "#q-t" >}} {{< pkgWeb "https://chris-prener.github.io/stlData" >}}
  - install the development version via GitHub - `devtools::install_github("chrisprener/stlData")`

## Tidyverse Packages
Use `install.packages("tidyverse")` to install these for convenience!

- `dplyr` - data wrangling {{< pkgIndex "#a-d" >}} {{< pkgCran "dplyr" >}} {{< pkgGitHub "tidyverse/dplyr" >}} {{< pkgWeb "http://dplyr.tidyverse.org/" >}} {{< pkgSheet "https://github.com/rstudio/cheatsheets/raw/master/data-transformation.pdf" >}} {{< pkgBook "http://r4ds.had.co.nz/transform.html" >}}
- `ggplot2` - data plotting {{< pkgIndex "#e-h" >}} {{< pkgCran "ggplot2" >}} {{< pkgGitHub "tidyverse/ggplot2" >}} {{< pkgWeb "http://ggplot2.tidyverse.org/" >}} {{< pkgSheet "https://github.com/rstudio/cheatsheets/raw/master/data-visualization-2.1.pdf" >}} {{< pkgBook "http://r4ds.had.co.nz/data-visualisation.html" >}}
  - install the development version via GitHub - `devtools::install_github("tidyverse/ggplot2")`
- `lubridate` - work with dates {{< pkgIndex "#i-l" >}} {{< pkgCran "lubridate" >}} {{< pkgGitHub "tidyverse/lubridate" >}} {{< pkgWeb "http://lubridate.tidyverse.org/" >}} {{< pkgSheet "https://github.com/rstudio/cheatsheets/raw/master/lubridate.pdf" >}} {{< pkgBook "http://r4ds.had.co.nz/dates-and-times.html" >}}
- `magrittr` - pipe operator {{< pkgIndex "#m-p" >}} {{< pkgCran "magrittr" >}} {{< pkgGitHub "tidyverse/magrittr" >}} {{< pkgWeb "http://magrittr.tidyverse.org/" >}} {{< pkgBook "http://r4ds.had.co.nz/pipes.html" >}}
- `reprex` - reproducible examples {{< pkgIndex "#q-t" >}} {{< pkgCran "reprex" >}} {{< pkgGitHub "tidyverse/reprex" >}} {{< pkgWeb "http://reprex.tidyverse.org/" >}}
  - install the development version via GitHub - `devtools::install_github("tidyverse/reprex")`
- `stringr` - work with strings {{< pkgIndex "#q-t" >}} {{< pkgCran "stringr" >}} {{< pkgGitHub "tidyverse/stringr" >}} {{< pkgWeb "http://stringr.tidyverse.org/" >}} {{< pkgSheet "https://github.com/rstudio/cheatsheets/raw/master/strings.pdf" >}} {{< pkgBook "http://r4ds.had.co.nz/strings.html" >}}
- `tidyr` - data wrangling {{< pkgIndex "#q-t" >}} {{< pkgCran "tidyr" >}} {{< pkgGitHub "tidyverse/tidyr" >}} {{< pkgWeb "http://tidyr.tidyverse.org/" >}} {{< pkgSheet "https://github.com/rstudio/cheatsheets/raw/master/data-transformation.pdf" >}} {{< pkgBook "http://r4ds.had.co.nz/relational-data.html" >}}

## Primary Mapping Packages
- `classInt` - data wrangling {{< pkgIndex "#a-d" >}} {{< pkgCran "classInt" >}} {{< pkgGitHub "r-spatial/classInt" >}}
- `leaflet` - interactive maps {{< pkgIndex "#i-l" >}} {{< pkgCran "leaflet" >}} {{< pkgGitHub "rstudio/leaflet" >}} {{< pkgWeb "https://rstudio.github.io/leaflet/" >}}
- `RColorBrewer` - color ramps for mapping {{< pkgIndex "#q-t" >}} {{< pkgCran "RColorBrewer" >}} {{< pkgWeb "http://colorbrewer2.org/" >}}
- `scales` - map scales {{< pkgIndex "#q-t" >}} {{< pkgCran "scales" >}}
- `sf` - spatial data tools {{< pkgIndex "#q-t" >}} {{< pkgCran "sf" >}} {{< pkgGitHub "r-spatial/sf" >}}
- `tidycensus` - census data tools {{< pkgIndex "#q-t" >}} {{< pkgCran "tidycensus" >}} {{< pkgGitHub "walkerke/tidycensus" >}} {{< pkgWeb "https://walkerke.github.io/tidycensus/" >}}
- `tigris` - census geography tools {{< pkgIndex "#q-t" >}} {{< pkgCran "tigris" >}} {{< pkgGitHub "walkerke/tigris" >}}

## Secondary Mapping Packages
*We may or may not be using these packages this semester!*

- `mapproj` - map projections {{< pkgIndex "#m-p" >}} {{< pkgCran "mapproj" >}}
- `maptools` - spatial data tools {{< pkgIndex "#m-p" >}} {{< pkgCran "maptools" >}}
- `rgeos` - spatial data tools {{< pkgIndex "#q-t" >}} {{< pkgCran "rgeos" >}}
- `rgdal` - spatial data tools {{< pkgIndex "#q-t" >}} {{< pkgCran "rgdal" >}}

## Other Packages
- `devtools` - install packages from GitHub {{< pkgIndex "#e-h" >}} {{< pkgCran "devtools" >}} {{< pkgGitHub "hadley/devtools" >}}
- `here` - working directory management {{< pkgIndex "#e-h" >}} {{< pkgCran "here" >}} {{< pkgGitHub "krlmlr/here" >}}
- `janitor` - data wrangling and tables {{< pkgIndex "#e-h" >}} {{< pkgCran "janitor" >}} {{< pkgGitHub "sfirke/janitor" >}}
  - install the development version via GitHub - `devtools::install_github("sfirke/janitor")`
- `knitr` - dynamic documents in `R` {{< pkgIndex "#i-l" >}} {{< pkgCran "knitr" >}} {{< pkgGitHub "yihui/knitr" >}} {{< pkgWeb "https://yihui.name/knitr/" >}} {{< pkgSheet "https://github.com/rstudio/cheatsheets/raw/master/rmarkdown-2.0.pdf" >}}
- `naniar` - missing data analysis {{< pkgIndex "#m-p" >}} {{< pkgCran "naniar" >}} {{< pkgGitHub "njtierney/naniar" >}} {{< pkgWeb "http://naniar.njtierney.com" >}}
- `RMarkdown` - markdown syntax for `R` {{< pkgIndex "#q-t" >}} {{< pkgCran "RMarkdown" >}} {{< pkgGitHub "rstudio/rmarkdown" >}} {{< pkgWeb "http://rmarkdown.rstudio.com/" >}} {{< pkgSheet "https://github.com/rstudio/cheatsheets/raw/master/rmarkdown-2.0.pdf" >}}