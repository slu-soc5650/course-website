+++
title = "Protecting Your Work"

date = 2018-12-05T00:00:00
lastmod = 2019-02-18T00:00:00

draft = false  # Is this a draft? true/false
toc = true  # Show table of contents? true/false
type = "docs"  # Do not modify.

# Add menu entry to sidebar.
linktitle = "Protecting Your Work"
[menu.docs]
  parent = "Fundamentals"
  weight = 3
+++

## Meta
<i class="meta-badge semester-sp19"><i class="far fa-calendar-alt fa-lg"></i>&nbsp; **Spring 2020** </i> 
<i class="meta-badge progress-full"><i class="fas fa-tasks fa-lg"></i>&nbsp; **Full** </i> 
<i class="meta-badge progress-update"><i class="far fa-clock fa-lg"></i>&nbsp; **2020-02-21** </i>

## Key Topics
<a class="meta-badge keyword" href="/docs/topic-index/#a-d"><i class="fas fa-tags fa-lg"></i>&nbsp; **Analysis development**</a>

## Overview
One of the biggest challenges to with doing computational work is that it requires a high degree of organization. Our approaches to file management on computers are often haphazard, with `Documents` and `Downloads` folders filled with disorganized files or a `Desktop` covered in dozens of files. Perhaps this has worked in the past, but that approach (or lack thereof) **will** fail students in this course. Moreover, if left un-checked, it will fail students down the road when a hard drive failure or natural disaster renders their data irrevocably inaccessible. This chapter covers what some of those threats are and ways to manage those risks when conducting computational research. 

## Threats To Our Data
Each semester that I teach [Introduction to GIS](https://slu-soc5650.github.io) and [Quantitative Analysis](https://slu-soc5050.github.io), several things happen. The first thing that happens is that students regularly lose files. The effects of losing files can range from being a minor frustration to a major headache depending on the file in question. Losing files often results in downloading multiple copies of the same data and recreating work. Both of these are wastes of your time. Moreover, files are rarely gone. They are typically just misplaced. This is bad for reproducibility, particularly when you happen across multiple versions of the same file and have to sort out which version is the version you last worked on.

The second thing that happens is that students who use thumb drives for data storage lose them. Depending on the timing of this loss, this can again range from being a minor frustration (very early in the semester) to being downright anxiety attack producing (last few weeks of the semester). Recreating an entire semester’s worth of work on the final project is both a tremendous waste of your time and a particularly unpleasant experience.

Fortunately, I have never had a student’s computer hard drive die during the course of the semester. However, I assume that if I teach this course long enough a hard drive failure will indeed occur. The backup provider [Backblaze](https://www.backblaze.com/) has [analyzed](https://www.backblaze.com/blog/how-long-do-disk-drives-last/) their own hard drives and found that about 5% of drives fail within the first year. After four years, a quarter (25%) of drives in their data center fail. Similarly, it is only a matter of time before a student’s computer is stolen along with all of their hard work. A less likely though still very plausible scenario involves the destruction of a student’s belongings (computer and thumb drive included) in a fire, car accident, or natural disaster.

Despite the likelihood that you will at some-point lose a thumb drive (if not during this semester than sometime down the road) and the near certainty that your computer’s hard drive will eventually fail if a rogue wave does not get it first, few students and faculty take these risks seriously. While you cannot prevent many of these things from happening, I want to suggest to you that you can take some simple steps to sure that *when* (not if) they happen, you are well prepared to get back to work with minimal disruption.

## Creating a Sustainable File System
The first thing that students can do to stave off problems with lost files is to actively and mindfully manage their files. In his excellent document [*The Plain Person’s Guide to Plain Text Social Science*](http://plain-text.co), Kieran Healy describes two important revolutions in computing that are currently taking place. One of them is the advent of mobile touch-screen devices, which he notes

> hide from the user both the workings of the operating system and (especially) the structure of the file system where items are stored and moved around.

For most users, I would argue that this extends to their laptop or desktop computers as well. I would venture to guess that the majority of my students are used to keeping large numbers of files on their desktops or in an (distressingly) disorganized `Documents` folder. For research, particularly quantitative research, such an approach to file management is unsustainable. It is difficult to produce *any* research, let alone work that is reproducible, without an active and mindful approach to file management.

### Create a *Single* Course Directory
The most successful approach to organizing files is to identify *one and only one* area that you will store course files in. Having files scattered around you hard drive between you `Desktop` directory, `Downloads`, `Documents`, and a half dozen other places is a recipe for lost files. It can also add complexity to the task of backing these files up. I recommend naming this directory simply based on the course you are enrolled in, either `SOC4650` or `SOC5650`. These names are short, have no punctuation or spaces (which can create conflicts with software), and explicitly connects the directory to this course as opposed to other courses you may take that are also GIS courses (a good reason to avoid naming the directory `GIS`!).

This single course directory should reside in *one and only one* place. Once you have these folders set-up, I want you to an agreement with yourself: files for the course will *only* be saved within this structure. Do not temporarily save files to the `Desktop`, for example, intending to move them later. They will be forgotten. Like New Years resolutions, it is easy to say that you will use a file system but difficult to maintain that promise when stress sets in or you are rushed. Do *everything* you can to maintain your file system.

### Storing the Course Directory
Storing this directory inside a sync'd directory (like Dropbox or Google Drive) may cause conflicts with your Git repositories. Instead, students for both of my courses are encouraged utilize a large sized thumb drive or an external hard drive for data storage (see the "Course Onboarding" section of the respective course's website for additional details). Having data stored on an external device raises the risk of physical loss, but also makes it easier to move work between different computers. This is particularly challenging for GI Science work, where spatial data sources can be may megabytes in size.

macOS users should make sure that the external drive is formatted using the ExFat file system specification so that it is readable both by their operating system and the Windows operating system in the computer lab. If you buy a new drive, you will likely have to re-format it. Directions for doing so are [available from Apple](https://support.apple.com/kb/PH22241?locale=en_US).

If you don't want to use a thumb drive, you will need to take extra care to keep your course materials spread across different computers in-sync.

### Approach Organizing Systematically
Within your single course directory, I recommend following a mindful, purposeful approach to organization. This approach begins with having a number of dedicated subfolders within your course directory:

```
/SOC4650
  /LectureExamples
  /Notes
  /Readings
```

Note again how these directories are named - there are no spaces, special characters, and the names are deliberately short but specific. For a directory with two words (e.g. `DataLibrary`), I use what is known as camelCase to name the file where the second (any any subsequent) words have their first character capitalized. You could also use dash-case (e.g. `Core-Documents`) or snake_case (e.g. `Core_Documents`) as a naming strategy. Regardless of which of these approaches you take, try to use it consistently.

Each folder in this example has a dedicated purpose:

* `LectureExamples` - a folder for creating projects specific to in-class examples during lectures
* `LectureRepos` - a folder for cloning lecture repositories into
* `Notes` - keep any class notes here
* `Readings` - keep and `.pdf` readings here

### Course Git Repos
The other set of materials you'll need to store are your course repositories. By default, these are saved by GitHub Desktop to the `Documents/GitHub/` path. For folks who are less comfortable with computers, I think it is fine to clone lecture repos as well as `DoeAssignments` (your assignments repository) and `DoeProject` (your final project repository). If you are more comfortable with computers, you may want to store these repos in your course folder so that everything is stored together.

## Organizing Projects
Following the excellent article [*Good enough practices in scientific computing*](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005510) (Wilson et al. 2017), I suggest data science projects should be organized in a specific, standardized way. This approach serves much the same purpose as the previous section on [Creating a Sustainable File System] - work that is well organized is better insured against loss. 

### A Sample Project - ArcGIS Pro Only
Much as I suggested above that course files reside in one and only one place, projects should be organized similarly (with one important caveat below). What follows is a sample project and then descriptions of each element. More details about each folder (excepting `maps`) can be found in the article. The project below contains all of key elements of a small geospatial research project that only uses ArcGIS Pro:

```
  /sample-project
    /data
      sample-project.gdb
      
      /rawtracts
        rawTracts.shp
        
    /ImportLog
    
    /Index
    
    /results
      map.png
      
    /source
      sample-project.tbx
      
    sample-project.aprx
    README.md
```

* The `data/` folder should contain all of the data needed for the project. For more complex assignments where you are created "clean" versions of the data, consider adding `data/raw/` and `data/clean/` subfolders. Once you're comfortable doing so, the geodatabase should also be moved to this folder.
* The `results/` folder should be used for all map outputs
* The `source/` folder should be used for your `.tbx` file, which is the ArcGIS Pro toolbox associated with your project.
* A `.aprx` file for your project
* A `README.md` file descibing the organization of your project

### A Sample Project - R Only
Similarly, this project only usese `R`. It has many of the same elements:

```
  /sample-project
    /data
      rawData.csv
      
      /rawtracts
        rawTracts.shp
        
    /docs
      notebook.md
      notebook.Rmd
      notebook.nb.html
      
    /results
      map.png
      
    /source
      script.R
      
    sample-project.Rproj
    README.md
```

* The `data/` folder should contain all of the data needed for the project. For more complex assignments where you are created "clean" versions of the data, consider adding `data/raw/` and `data/clean/` subfolders. 
* The `docs/` folder should be used for all `.Rmd` files and their output
* The `results/` folder should be used for all map outputs
* The `source/` folder should be used for any scripts you might need (these will be few and far between, if any, in this course)
* A `.Rproj` file for your project
* A `README.md` file descibing the organization of your project

### A Sample Project - A Combined `R` and ArcGIS Pro Project
Here is what a full project that uses both ArcGIS Pro and `R` might look like:

```
  /sample-project
    /data
      rawData.csv
      sample-project.gdb
      
      /rawtracts
        rawTracts.shp
        
    /docs
      notebook.md
      notebook.Rmd
      notebook.nb.html

    /ImportLog
    
    /Index
    
    /results
      map.png
      
    /source
      sample-project.tbx
      script.R
      
    sample-project.aprx
    sample-project.Rproj
    README.md
```

## Backing Up Your Data
All of the organization in the world cannot prevent a computer hard drive from failing or a natural disaster from destroying your hardware. Similarly, even the best organized of us lose things sometimes or accidentally delete files. Backing up files is therefore a critical piece of not just doing computational work but, in this day and age, it is a requisite skill for owning computer hardware. Every device you own including your phone can and should be backed up. There are a number of different ways to think about backing up your data. The most successful backup strategies will incorporate all of these three elements.

### Bootable Backups
“Bootable” backups are mirrored images of your *entire* hard drive, down to temporary files, icons, and system files. With a bootable backup, you can restore your entire computer in the event of a hard drive failure or a corruption of the operating system files. They are named as such because you can plug in the external drive that you are using for this backup and literally boot your computer up from that drive (typically a *very* slow process).

These backups are often made less frequently because they can be resource intensive and it is best not to use your operating system while creating a clone. They are typically made to an external hard drive, which is subject to similar failure rates as the hard drives inside your computer. So bootable drives need to be replaced every few years to maintain their reliability.

Both major operating systems come with applications for creating clones of your main hard drive that are bootable, and there are a number of third party applications that provide this service as well.

### Incremental Backups
Incremental backups are designed to keep multiple copies of a single file (how often depends on the type of software you use and the settings you select). These can be used to restore an older copy of a file if work is lost or a newer file is corrupted.

Apple’s TimeMachine is a great example of an incremental backup - when kept on, it creates hourly backups of files that have been changed, daily backups for the previous month, and weekly backups for previous months. Once the disk is full, the oldest backups are deleted. Dropbox also provides a similar service, retaining all previous versions of files (and deleted files) for thirty days.

Incremental backups are typically good options for recovering files that have been recently changed (again, depending on the software you use and the settings you select). Since they run frequently (every time a file is changed or every hour, for example), recent changes tend to get captured. They can be limited in terms of their long-term storage - it may not be possible to recover older versions of a file past a few weeks.

They are also not always good solutions for recreating your entire computer since they do not save all necessary program and operating system files, and may be cumbersome to work with if you need to recover a large quantity of files. Like bootable backups, these are typically stored on external hard drives that need to be replaced on a regular basis.

In addition to the aforementioned Apple TimeMachine, the Windows OS also comes with a built-in service for creating incremental backups. Dropbox is a good option if you have a small number of files, but you may find the need to upgrade to a paid account if you have a large amount of data.

### Cloud Backups
Cloud backup services like [Backblaze](https://www.backblaze.com) or [Crashplan](https://www.code42.com/crashplan/) offer comprehensive backup solutions for customers. These plans typically require a monthly subscription fee to maintain access to your backups. While bootable backups protect against hard drive failure and incremental backups protect against data corruption, cloud backups protect against catastrophic events like robberies, fires, and other natural disasters. A fire or a tornado that affect your house may destroy your laptop and any external hard drives you use for backup, but your cloud backup will be unaffected.

### A Workflow for Backups
Just as we need a workflow for approaching file management, it is also important to establish a routine for backups. With backups, the most successful workflows are those that require next to no effort on your part. If you primarily use a desktop, this can be as simple as leaving two external hard drives plugged into your computer since most backup software can be set to run automatically. If you have tasks that require you to manually do something (plug an external hard drive into your computer, for instance), create a reminder for yourself on a paper calendar or a digital calendar or to-do list application.

{{% alert note %}}
I gave a presentation on workflows for backing data up as part of the [Data Science Seminar](https://slu-dss.github.io) series at [Saint Louis University](https://slu.edu). You can easily view the slides from that presentation on [Speaker Deck](https://speakerdeck.com/chrisprener/protecting-your-data), and you can download the session's materials from [GitHub](https://github.com/slu-dss/protectData).
{{% /alert %}}

For this course in particular, it is *imperative* that you backup the data on your flash drive. A number of possibilities exist for accomplishing this:

  - Keep a local copy of your flash drive's files on your computer.
  - Keep a `.zip` archive of your files in a service like Dropbox or Google Drive. (Using a `.zip` archive will prevent issues with your `.git` repositories.)
  - Maintain a second flash drive copies of all of your files.

Whatever solution you select, make sure you regularly update your backup. The more often you keep your backup archive updated, the less stressful and disruptive losing your drive will be. This will likely be a manual task, so follow the guidance above about creating a repeating calendar event or to-do list task reminder.