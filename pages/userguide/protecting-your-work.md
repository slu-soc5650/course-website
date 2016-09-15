---
layout: page
title: User's Guide
tagline: Protecting Your Work
tags: [GitHub, Stata]
description:
---

Each semester that I teach SOC 5050 or SOC 5650 (Intro to GIS), two things happen. The first thing that happens is that students regularly lose files. The effects of losing files can range from being a minor frustration to a major headache depending on the file in question. Losing files often results in downloading multiple copies of the same data and recreating work. Both of these are wastes of your time. Moreover, files are rarely gone. They are typically just misplaced. This is bad for reproducibility, particularly when you happen across multiple versions of the same file and have to sort out which
version is the version you last worked on.

The second thing that happens is that students lose their thumb drives. Depending on the timing of this loss, this can again range from being a minor frustration (very early in the semester) to being downright anxiety attack producing (last few weeks of the semester). Recreating an entire semester’s worth of work on the final project is both a tremendous waste of your time and a particularly unpleasant experience. We will not be using thumb drives as a matter of class policy in this class (unlike SOC 5650), but the challenge they present serves as a teachable moment.

Fortunately, I have never had a student’s computer hard drive die during the course of the semester. However, I assume that if I teach this course long enough a hard drive failure will indeed occur. The backup provider [Backblaze](https://www.backblaze.com/) has [analyzed](https://www.backblaze.com/blog/how-long-do-disk-drives-last/) their own hard drives and found that about 5% of drives fail within the first year. After four years, a quarter (25%) of drives in their data center fail.

Similarly, it is only a matter of time before a student’s computer is stolen along with all of their hard work. A less likely though still very plausible scenario involves the destruction of a student’s belongings (computer and thumb drive included) in a fire, car accident, flood, earthquake, tornado, hurricane, avalanche, or mudslide.

Despite the likelihood that you will at some-point lose a thumb drive (if not during this semester than sometime down the road) and the near certainty that your computer’s hard drive will eventually fail if a rogue wave does not get it first, few students and faculty take these risks seriously. While you cannot prevent many of these things from happening, I want to suggest to you that you can take some simple steps to sure that *when* (not if) they happen, you are well prepared to get back to work with minimal disruption.

### Creating a Sustainable File System
In his excellent document [*The Plain Person’s Guide to Plain Text Social Science*](http://plain-text.co), Kieran Healy describes two important revolutions in computing that are currently taking place. One of them is the advent of mobile touch-screen devices, which he notes

> hide from the user both the workings of the operating system and (especially) the structure of the file system where items are stored and moved around.

For most users, I would argue that this extends to their laptop or desktop computers as well. I would venture to guess that the majority of my students are used to keeping large numbers of files on their desktops or in an (distressingly) disorganized `Documents` folder.

For research, particularly quantitative research, such an approach to file management is unsustainable. It is difficult to produce *any* research, let alone work that is reproducible, without an active approach to file management.

#### Create a *Single* Course Directory
With one major exception (see the secontion below on GitHub), the most successful approach to organizing files is to identify *one and only one* area that you will store course files in. Having files scattered around you hard drive between you `Desktop` directory, `Downloads`, `Documents`, and a half dozen other places is a recipe for lost files. It can also add complexity to the task of backing these files up. I recommend naming this directory simply `SOC5050`. This is short, has no punctuation or spaces (which can create conflicts with software), and explicitly connects the directory to this course as opposed to other courses you may take that are also statistics courses (a good reason to avoid naming the directory `Statistics`!).

#### Approach Organizing Systematically
Within your single course directory, I recommend following much of Long's (2009) advice on organization. Approach this task systematically and mindfully. This approach begins with having a number of dedicated subfolders within your course directory:

```
/SOC5050
  /CoreDocuments
  /Data
  /FinalProject
  /GitHub
  /Notes
  /Posted
  /Readings
  /Working
```
Note again how these directories are named - there are no spaces, special characters, and the names are deliberately short but specific. For a directory with two words (`CoreDocuments` or `FinalProject`), I use what is known as camelCase to name the file where the second (any any subsequent) words have their first character capitalized. You could also use dash-case (`Core-Documents`) or snake_case (`Core_Documents`) as a naming strategy.

A `.zip` file containing an empty folder structure that mirrors what is described below will be posted to GitHub early in the semester.

##### The `CoreDocuments` Directory
This directory should be used to store *copies* of the core documents repository files that you sync from GitHub - the Syllabus, the Reading List, and the User's Guide. The files on GitHub may be updated (and therefore updated on your computer when you sync), so having local copies that are independent of GitHub can be helpful if you want to make sure you retain original files.

##### The `Data` Directory
The data directory should have copies of all original data and their documentation. I recommend renaming the files that you download from Dropbox for simplicity (most files come from the [ICPSR data repository](http://www.icpsr.umich.edu/icpsrweb/), which has a complex standard for file naming) and removing some files from the `CPS` and `NHIS` directories:

```
/SOC5050
  /Data
    /Acock
    /CPS
      /cpsCodebook.pdf
      /cpsDescription.pdf
      /cpsOriginalData.dta
      /cpsUserGuide.pdf
    /Long
    /NHIS
```
Note that the 2012 General Social Survey has been removed - I keep that in the `FinalProject` directory (see below).

##### The `FinalProject` Directory
The final project directory should be a microcosm of the larger directory structure, with most major directories replicated so that your final project files have a dedicated, organized home:

```
  /SOC5050
    /FinalProject
      /Data
        /gssCodebook.pdf
        /gssDescription.pdf
        /gssDocumentation.pdf
        /gssOriginalData.dta
        /gssQuestionarrie.pdf
        /gssRelatedLiterature.txt
        /gssReportQuickFacks.pdf      
      /Directions
      /Notes
      /Posted
      /Readings
      /Working
```
I recommend keeping subdirectories within posted dedicated for different versions of your data analysis, paper, and presentation files.

I also recommend using some type of bibliography software ([Endnote](http://endnote.com), for example, can be obtained for free by SLU students). Whatever application you choose, keep its primary database for your project in the `Readings` folder along with copies of all `.pdf` readings.

You will also be asked to create and maintain a research log for this project (see Long [2009]). I recommend keeping this and any other project notes in the `Notes` directory.

Details on the `Posted` and `Working` directories can be found below. You should replicate the practices that feed these directories for your final project.

##### The `GitHub` directory
This directory should contain the local copies of the repositories that you sync from GitHub's servers:

```
  /SOC5050
    /GitHub
      /Core-Documents
      /PrenerAssignments
      /Week-01
      /Week-02
      ...
      /Week-15
```
You should clone and then sync the Core-Documents repository, your assignment repository, and all weekly repositories.

You will be in-charge of organizing the assignments repository. I recommend creating a subfolder for your final project deliverables, a subfolder for labs, and a subfolder for problem sets. Within those subfolders, create individual directories for assignments:

```
  /SOC5050
    /GitHub
      /DoeAssignments
        /FinalProject
          /Drafts
          /Final
          /LiteratureReview
          /Memo
        /Labs
          /Lab01
          /Lab02
          ...
          /Lab16
        /ProblemSets
          /PS01
          /PS02
          ...
          /PS10
```
There are two important things to keep in mind about about your GitHub directory:
  1. The first will only apply to students whose backup strategy involves using **Dropbox** or **Google Drive** to sync their course directory with a cloud storage service. If you do this, you **must** keep local copies of GitHub repositories outside of your course directory. GitHub uses software called Git for version tracking, and Git files (which are hidden from your view if you look at the directories in Apple's Finder or Windows Explorer) do not mix well with the version tracking software embedded in Dropbox and Google Drive.
  2. Do not edit the files in these repositories - copy them to your working folder (or other relevant destination) and then edit versions. Editing files in the `Core-Documents` or weekly directories may create sync conflicts, and your assignments directory should be dedicated to *completed* and *posted* files that are required for submission.

##### The `Notes` Directory
Use this as a home for course notes and other resources.

##### The `Posted` Directory
I use this the way Long (2009) suggests - once a particular set of assignments, analyses, or writing is completed, I save it in a subfile within the `Posted` directory:

```
  /SOC5050
    /Posted
      /Lab01
      /Lab02
      /PS01
```
These contain all of the files needed for an assignment and not just the deliverables requested for submission. Follow Long's (2009) advice - one files are saved in the `Posted` directory, do not edit them again. Copy any necessary data or other files out of the directory into the working directory, and edit them here. Once you are done, save them in a new subfolder within the `Posted` directory.

##### The `Readings` Directory
Use this as a home for `.pdf` copies of course readings.

##### The `Working` Directory
As with the `Posted` directory, I suggest following Long's (2009) advice and using this as a temporary holding place for files you are working on. Once they are done, move them out of the `Working` directory immediately and into a subfolder within the `Posted` directory.

### Backing Up Your Data
There are a number of different ways to think about backing up your data. The most successful backup strategies will incorporate all of these elements.

#### Bootable Backups
“Bootable” backups are mirrored images of your *entire* hard drive, down to temporary files, icons, and system files. With a bootable backup, you can restore your entire computer in the event of a hard drive failure or a corruption of the operating system files. They are named as such because you can plug in the external drive that you are using for this backup and literally boot your computer up from that drive (typically a *very* slow process).

These backups are often made less frequently because they can be resource intensive and it is best not to use your operating system while creating a clone. They are typically made to an external hard drive, which is subject to similar failure rates as the hard drives inside your computer. So bootable drives need to be replaced every few years to maintain their reliability.

Both major operating systems come with applications for creating clones of your main hard drive that are bootable, and there are a number of third party applications that provide this service as well.

#### Incremental Backups
Incremental backups are designed to keep multiple copies of a single file (how often depends on the type of software you use and the settings you select). These can be used to restore an older copy of a file if work is lost or a newer file is corrupted.

Apple’s TimeMachine is a great example of an incremental backup - when kept on, it creates hourly backups of files that have been changed, daily backups for the previous month, and weekly backups for previous months. Once the disk is full, the oldest backups are deleted. Dropbox also provides a similar service, retaining all previous versions of files (and deleted files) for thirty days.

Incremental backups are typically good options for recovering files that have been recently changed (again, depending on the software you use and the settings you select). Since they run frequently (every time a file is changed or every hour, for example), recent changes tend to get captured. They can be limited in terms of their long-term storage - it may not be possible to recover older versions of a file past a few weeks.

They are also not always good solutions for recreating your entire computer since they do not save all necessary program and operating system files, and may be cumbersome to work with if you need to recover a large quantity of files. Like bootable backups, these are typically stored on external hard drives that need to be replaced on a regular basis.

In addition to the aforementioned Apple TimeMachine, the Windows OS also comes with a built-in service for creating incremental backups. Dropbox is a good option if you have a small number of files, but you may find the need to upgrade to a paid account if you have a large amount of data.

#### Cloud Backups
Cloud backup services like [Backblaze](https://www.backblaze.com) or [Crashplan](https://www.code42.com/crashplan/) offer comprehensive backup solutions for customers. These plans typically require a monthly subscription fee to maintain access to your backups. While bootable backups protect against hard drive failure and incremental backups protect against data corruption, cloud backups protect against catastrophic events like robberies, fires, and other natural disasters. A fire or a tornado that affect your house may destroy your laptop and any external hard drives you use for backup, but your cloud backup will be unaffected.

#### A Workflow for Backups
Just as we need a workflow for approaching file management, it is also important to establish a routine for backups. With backups, the most successful workflows are those that require next to no effort on your part. If you primarily use a desktop, this can be as simple as leaving two external hard drives plugged into your computer since most backup software can be set to run automatically. If you have tasks that require you to manually do something (plug an external hard drive into your computer, for instance), create a reminder for yourself on a paper calendar or a digital calendar or to-do list application.

----

##### [Back to User's Guide Cover Page]({{ base }}/pages/user-guide.html)
