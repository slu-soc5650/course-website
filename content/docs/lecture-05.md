+++
title = "Lecture-05 - Map Production in R"

date = 2018-02-07T00:00:00
lastmod = 2019-02-12T00:00:00

draft = false  # Is this a draft? true/false
toc = true  # Show table of contents? true/false
type = "docs"  # Do not modify.

# Add menu entry to sidebar.
linktitle = "Lecture-05 - Map Production in R"
[menu.docs]
  parent = "Lectures"
  weight = 7
+++

## Meta
<i class="meta-badge semester-sp19"><i class="far fa-calendar-alt fa-lg"></i>&nbsp; **Spring 2019** </i> 
<i class="meta-badge progress-lecture"><i class="fas fa-tasks fa-lg"></i>&nbsp; **Lecture** </i> 
<i class="meta-badge progress-update"><i class="far fa-clock fa-lg"></i>&nbsp; **2019-02-17** </i>

## Key Topics
<a class="meta-badge keyword" href="/docs/topic-index/#a-d"><i class="fas fa-tags fa-lg"></i>&nbsp; **Analysis development**</a> 
<a class="meta-badge package" href="/docs/topic-index/#a-d"><i class="fas fa-archive fa-lg"></i> **base**</a> 
<a class="meta-badge keyword" href="/docs/topic-index/#a-d"><i class="fas fa-tags fa-lg"></i>&nbsp; **Cartography**</a> 
<a class="meta-badge package" href="/docs/topic-index/#e-h"><i class="fas fa-archive fa-lg"></i> **here**</a> 
<a class="meta-badge keyword" href="/docs/topic-index/#i-l"><i class="fas fa-tags fa-lg"></i>&nbsp; **Interactive maps**</a> 
<a class="meta-badge package" href="/docs/topic-index/#i-l"><i class="fas fa-archive fa-lg"></i> **leaflet**</a>
<a class="meta-badge package" href="/docs/topic-index/#i-l"><i class="fas fa-archive fa-lg"></i> **knitr**</a>
<a class="meta-badge tool" href="/docs/topic-index/#q-t"><i class="fas fa-wrench fa-lg"></i>&nbsp; **R**</a>
<a class="meta-badge package" href="/docs/topic-index/#q-t"><i class="fas fa-archive fa-lg"></i> **RMarkdown**</a>
<a class="meta-badge package" href="/docs/topic-index/#q-t"><i class="fas fa-archive fa-lg"></i> **sf**</a>
<a class="meta-badge package" href="/docs/topic-index/#u-z"><i class="fas fa-archive fa-lg"></i> **webshot**</a>

## Resources
<a class="btn btn-outline-primary resource" href="https://slu-soc5650.github.io/syllabus/lecture-05-map-production-in-r.html" target="_blank"><i class="fas fa-book fa-lg"></i>&nbsp; View on Syllabus </a> 
<a class="btn btn-outline-primary resource" href="https://github.com/slu-soc5650/lecture-05" target="_blank"><i class="fab fa-github fa-lg"></i>&nbsp; View on GitHub </a> 
<a class="btn btn-outline-primary resource" href="https://slu.tegrity.com/#/recording/0114fd3f-6ac2-4013-b5d2-c6cbd04cfd17" target="_blank"><i class="fas fa-video fa-lg"></i>&nbsp; View Recording </a>
<a class="btn btn-outline-primary resource" href="http://slu-soc5650.github.io/lecture-05/index.nb.html" target="_blank"><i class="fab fa-markdown fa-lg"></i>&nbsp; View Lecture Notebook </a>
<a class="btn btn-outline-primary resource" href="https://goo.gl/forms/HCfCVSrdglBfPcpi1" target="_blank"><i class="fab fa-google fa-lg"></i>&nbsp; eTicket-05 </a>
<a class="btn btn-outline-primary resource" href="https://github.com/slu-soc5650/lecture-05/blob/master/handouts/lecture-05-RStudio.pdf" target="_blank"><i class="fas fa-file-pdf fa-lg"></i>&nbsp; Handout - RStudio </a>
<a class="btn btn-outline-primary resource" href="https://github.com/slu-soc5650/lecture-05/blob/master/handouts/lecture-05-rMarkdown.pdf" target="_blank"><i class="fas fa-file-pdf fa-lg"></i>&nbsp; Handout - R Markdown </a>
<a class="btn btn-outline-primary resource" href="https://github.com/slu-soc5650/lecture-05/blob/master/assignments/lab-04.pdf" target="_blank"><i class="fas fa-file-pdf fa-lg"></i>&nbsp; Lab-04 </a>
<a class="btn btn-outline-primary resource" href="https://github.com/slu-soc5650/lecture-05/blob/master/assignments/lab-04-replication/" target="_blank"><i class="fas fa-folder-open fa-lg"></i>&nbsp; Lab-04 Replication </a>
<a class="btn btn-outline-primary resource" href="https://github.com/slu-soc5650/lecture-05/blob/master/assignments/ps-02.pdf" target="_blank"><i class="fas fa-file-pdf fa-lg"></i>&nbsp; PS-02 </a>
<a class="btn btn-outline-primary resource" href="https://github.com/slu-soc5650/lecture-05/blob/master/handouts/lecture-05-rProjectWorkflow.pdf" target="_blank"><i class="fas fa-file-pdf fa-lg"></i>&nbsp; Workflow - R Projects </a>

## Example of Live Leaflet Map
I've added a version of the map we created last night to the course docs along with all of the code I used to create it. Click on the image below to check it out!
<p> </p>
[![leaflet-example](/images/leaflet-example.png)](/docs/leaflet-example/)
<p> </p>