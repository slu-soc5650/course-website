+++
title = "Opinionated Tools and Processes"

date = 2018-12-05T00:00:00
lastmod = 2018-12-09T00:00:00

draft = false  # Is this a draft? true/false
toc = true  # Show table of contents? true/false
type = "docs"  # Do not modify.

# Add menu entry to sidebar.
linktitle = "Opinionated Tools and Processes"
[menu.docs]
  parent = "Fundamentals"
  weight = 1
+++

## Meta 
<i class="meta-badge semester-sp19"><i class="far fa-calendar-alt fa-lg"></i>&nbsp; **Spring 2019** </i> <i class="meta-badge progress-draft"><i class="fas fa-tasks fa-lg"></i>&nbsp; **Draft** </i> <i class="meta-badge progress-update"><i class="far fa-clock fa-lg"></i>&nbsp; **2018-12-09** </i>

## Key Topics
<a class="meta-badge keyword" href="/docs/topic-index/#a-d"><i class="fas fa-tags fa-lg"></i>&nbsp; **Analysis development**</a>

## Overview
The methods introduced in this course are meant to be "opinionated" - we start from a strong conception about what "good" geospatial data science looks like. I want to introduce a high level definition of opinionated processes here, and discuss how these ideas might fit into previous coursework you've taken as well as this one.

## Opinionated Processes
The idea of research being opinionated is something I borrow from [Hiliary Parker](https://twitter.com/hspter), who has been developing the idea of ["opinionated analysis development"](https://peerj.com/preprints/3210/) over the last several years. Parker (2017) argues that opinionated analysis development is a guard against human errors in data analysis that are common but preventable. She emphasizes process repeatedly because, in her view, errors in data analysis are often the result of poor process (and not the individual failures of an analyst). 

Following Hilary's lead, we will also make process a cornerstone of our coursework. This emphasis on process is not routine in research methods courses (Long 2009), which often treat methods and techniques in isolation and leave much about how they fit together to be learned "the hard way". A common experience with statistics coursework is that students will learn the assumptions and requirements of various tests, but not how to fit them together to produce a well-conceptualized analysis. Thus, students working on their first research projects often feel personal responsibility for errors "despite not being taught processes that protect against them" (Parker 2017:2).

Parker (2017) lays out three core areas for analysis development. Analyses should be:

1. reproducible and auditable, 
2. accurate, and 
3. collaborative. 

She also provides a set of opinions and questions about each of these these categories. Projects that are both reproducible and auditable, for example, should be driven by executable analysis scripts with clearly defined dependencies. Projects that are accurate should use modular, tested code and should assertively test data, assumptions, and results. Finally, projects that are collaborative should use version control software for project management, should have the ability to track issues, and should allow for communications that can be archived easily. Many of these same core ideas appear in the article on ["Good Enough" Research Practices](/docs/good-enough-practices).

## Opinionated Tools
TBD

## Contextualizing These Ideas
Each time I teach a research methods course, I have students with a mix of experiences. For some students, all of these concepts and techniques are new and they therefore do not have a strong conception of what it means to do research. For other students, particularly those with research experience, these ideas can directly conflict with how they have been taught in the past and how they work. For everyone, these ideas require a greater mindfulness and attention to detail than they are used to. 

Occasionally, students react strongly to these ideas. For example, these opinions could be interpreted as an indictment of students' own processes or seen as a desire to micromanage. Others could see the focus on process as misplaced. After all, as long as the final product looks good, what does it matter how organized the analyst's hard drive is (or isn't)? If you feel like this at any point in the semester, I can sympathize greatly. I remember the frustration I felt the first time I was told that I didn't name variables well and that my code was written in a way that was hard to read. 

What I didn't understand at the time, and what I strive to emphasize now, is that process cannot be separated from product. If the process is unclear, undefined, or disorganized, our faith in the final product should be diminished because these flaws limit our ability to judge its accuracy. Thus being "right" is not solely a judgement of the final results but also how they were obtained. This emphasis on process is inherently more time consuming, slower, and more deliberate than a slapdash approach to data analysis. Our goal is not to conduct data science work in the easiest way, however, it is to conduct it in the most robust way possible.
