+++
title = "Course Software"

date = 2018-12-04T00:00:00
lastmod = 2018-12-04T00:00:00

draft = false  # Is this a draft? true/false
toc = true  # Show table of contents? true/false
type = "docs"  # Do not modify.

# Add menu entry to sidebar.
linktitle = "Course Software"
[menu.docs]
  parent = "First Steps"
  weight = 2
+++

## Meta 
<i class="meta-badge semester-sp19"><i class="far fa-calendar-alt fa-lg"></i>&nbsp; **Spring 2019** </i> <i class="meta-badge progress-draft"><i class="fas fa-tasks fa-lg"></i>&nbsp; **Draft** </i> <i class="meta-badge progress-update"><i class="far fa-clock fa-lg"></i>&nbsp; **2018-12-04** </i>

## Overview
This course is built primarily around a set of four software applications - ArcGIS Pro, the programming language `R`, the graphical user interface for `R` called RStudio, and GitHub Desktop. As I noted on the [course onboarding page](/docs/course-onboarding), there are two choices for *accessing* software. Please read through the [course onboarding page](/docs/course-onboarding) page carefully and make the decisions you think are best for you - either using your own computer or using a lab computer. Feel free to shoot me an email if you have questions about which approach is best.

## ArcGIS Pro
{{% alert note %}}
ArcGIS Pro is installed in the GIS lab.
{{% /alert %}}

I am able to provide licenses for ArcGIS Pro to students who are interested in obtaining them. If you would like a license, please [check the system requirements](http://pro.arcgis.com/en/pro-app/get-started/arcgis-pro-system-requirements.htm) first. If your computer meets the minimum requirements, email me for a license. Then:

1. Visit ESRI's [education edition website](http://www.esri.com/educationedition) to begin the process of activating and downloading your ArcGIS Pro Student Trial software.
2. Log in using your **Existing Esri account** (the same one you were given during the [course onboarding process](/docs/course-onboarding)).
3. Enter the license code and click Activate ArcGIS.
4. Click the button for the ArcGIS for Desktop software version being activated - the latest version of ArcGIS Pro.
5. If necessary, download the ArcGIS Uninstall Utility and uninstall previous versions of ArcGIS Desktop or ArcGIS Pro.
6. Run the executable file that you downloaded to install ArcGIS Pro.

## Spatial Libraries
{{% alert note %}}
These libraries are installed in the GIS lab.
{{% /alert %}}

There are three open-source spatial libraries that we will indirectly use this semester - GDAL, GEOS, and PROJ.4. They'll be used by the `R` package `sf`.

### Windows
To install the libraries on Windows, you need to have [RTools](https://cran.r-project.org/bin/windows/Rtools/) installed. RTools is a suite of tools for building packages on Windows, and it will allow sf to install a number of spatial data libraries that it requires to read and process shapefiles. These tools require administrative rights, so you may have to enter your password.

### macOS
Users on macOS will have to install the spatial data libraries on their own. An omnibus installer is available from the [Kyng Chaos website](https://www.kyngchaos.com/software/frameworks) - you'll want to download and run the GDAL 2.2 Complete installer. 

## R
### Installing Base R
{{% alert note %}}
Base R is installed in the GIS lab.
{{% /alert %}}

You can download `R` from its [website](https://cloud.r-project.org). Choose "Download R for (Mac) OS X" or "Download R for Windows". Windows users should look for text that says "install R for the first time" and click the `base` to the left of that text. Both macOS and Windows users should install `R` version 3.5.1, known as "Feather Spray". 

If you already have `R` installed, please make sure you have the latest version. You can upgrade it using the same process for a new installation.

### Installing R Packages
{{% alert warning %}}
R packages will need be installed both in the lab and on personal computers.
{{% /alert %}}

There are a number of `R` packages that you will need for this semester. If you feel feel comfortable, go ahead and take care of this before the semester starts. If not, we'll go over how to do this type of installation on the first day of class!

The following code snipped can be pasted into your `R` console to install all of these required packages.

```
install.packages(c("tidyverse", "janitor", "sf", 
    "stldata", "testDriveR"))
```

Depending on your version of `R` and your operating system, there will be other dependencies that are required and the number of packages installed will be considerably larger. The installation process has not been extensively tested on different operating system and hardware configurations, and though it is unlikely, you may encounter issues. If you do, please let Chris know!

## RStudio
{{% alert note %}}
RStudio is installed in the GIS lab.
{{% /alert %}}

RStudio is a graphical user interface for `R` that will make learning the language and using it much, much easier. You should download the *free* version of RStudio from [their website](https://www.rstudio.com/products/rstudio/download/#download). Choose the appropriate installer for your platform. Make sure `R` is already installed before installing RStudio. 

If you already have RStudio installed, please make sure you have the latest version. You can upgrade it using the same process for a new installation.

## GitHub Desktop
{{% alert warning %}}
GitHub Desktop will need be installed both in the lab and on personal computers.
{{% /alert %}}

In addition to the applications above, everyone will need a local installation of GitHub Desktop, which is a graphical user interface for accessing Git and GitHub.com. It can be downloaded for free from the [application's website](https://desktop.github.com). You will need to download and run the installer. Once it is complete, you will need to login to the application with your [GitHub.com username and password](/docs/onboarding). 

If you already have GitHub Desktop installed, you should check to make sure you are running the latest version of GitHub Desktop. If you need to update GitHub Desktop, you should also [download](https://git-scm.com/downloads).

## Other Applications
You can download mobile apps for our forum software, Discourse, for both [iOS](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=2&cad=rja&uact=8&ved=2ahUKEwiY686XhYffAhWiVN8KHU64CJYQFjABegQIABAB&url=https%3A%2F%2Fitunes.apple.com%2Fus%2Fapp%2Fdiscourse-app%2Fid1173672076&usg=AOvVaw07B3SNCMe5L2b0byHxYb7p) and [Android](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=1&cad=rja&uact=8&ved=2ahUKEwiY686XhYffAhWiVN8KHU64CJYQFjAAegQICBAB&url=https%3A%2F%2Fplay.google.com%2Fstore%2Fapps%2Fdetails%3Fid%3Dcom.discourse%26hl%3Den_US&usg=AOvVaw3WxkdpwbRAazq0PByDxG7-) devices.
