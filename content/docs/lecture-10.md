+++
title = "Lecture-10 - Projections"

date = 2018-03-18T00:00:00
lastmod = 2019-03-25T00:00:00

draft = false  # Is this a draft? true/false
toc = true  # Show table of contents? true/false
type = "docs"  # Do not modify.

# Add menu entry to sidebar.
linktitle = "Lecture-10 - Projections"
[menu.docs]
  parent = "Lectures"
  weight = 9
+++

## Meta
<i class="meta-badge semester-sp19"><i class="far fa-calendar-alt fa-lg"></i>&nbsp; **Spring 2019** </i> 
<i class="meta-badge progress-full"><i class="fas fa-tasks fa-lg"></i>&nbsp; **Full** </i> 
<i class="meta-badge progress-update"><i class="far fa-clock fa-lg"></i>&nbsp; **2019-03-25** </i>

## Key Topics
<a class="meta-badge tool" href="/docs/topic-index/#a-d"><i class="fas fa-wrench fa-lg"></i>&nbsp; **ArcGIS Pro**</a>
<a class="meta-badge keyword" href="/docs/topic-index/#m-p"><i class="fas fa-tags fa-lg"></i>&nbsp; **Projections**</a> 
<a class="meta-badge tool" href="/docs/topic-index/#q-t"><i class="fas fa-wrench fa-lg"></i>&nbsp; **R**</a>
<a class="meta-badge keyword" href="/docs/topic-index/#q-t"><i class="fas fa-tags fa-lg"></i>&nbsp; **Select by location**</a>
<a class="meta-badge package" href="/docs/topic-index/#q-t"><i class="fas fa-archive fa-lg"></i> **sf**</a>

## Resources
<a class="btn btn-outline-primary resource" href="https://slu-soc5650.github.io/syllabus/lecture-10-projections.html" target="_blank"><i class="fas fa-book fa-lg"></i>&nbsp; View on Syllabus </a> 
<a class="btn btn-outline-primary resource" href="https://github.com/slu-soc5650/lecture-10" target="_blank"><i class="fab fa-github fa-lg"></i>&nbsp; View on GitHub </a> 
<a class="btn btn-outline-primary resource" href="http://slu-soc5650.github.io/lecture-10/index.nb.html" target="_blank"><i class="fab fa-markdown fa-lg"></i>&nbsp; View Lecture Notebook </a>
<a class="btn btn-outline-primary resource" href="https://goo.gl/forms/scxILPmkXJjtcQr72" target="_blank"><i class="fab fa-google fa-lg"></i>&nbsp; eTicket-10 </a>
<a class="btn btn-outline-primary resource" href="https://github.com/slu-soc5650/lecture-10/blob/master/assignments/lab-09.pdf" target="_blank"><i class="fas fa-file-pdf fa-lg"></i>&nbsp; Lab-09 </a>
<a class="btn btn-outline-primary resource" href="https://github.com/slu-soc5650/lecture-10/blob/master/assignments/lab-09-replication/" target="_blank"><i class="fas fa-folder-open fa-lg"></i>&nbsp; Lab-09 Replication </a>

## Lecture Slides
<p> </p>
<script async class="speakerdeck-embed" data-id="b5ad8a7638cd441c8e1d4f95dc169454" data-ratio="1.33333333333333" src="//speakerdeck.com/assets/embed.js"></script>
<p> </p>

## Lab-09 Replication Slides
<p> </p>
<script async class="speakerdeck-embed" data-id="8ee2961aeba546af9a1f9d016341a200" data-ratio="1.33333333333333" src="//speakerdeck.com/assets/embed.js"></script>
<p> </p>

## Key Websites
There are two good reference websites that contain cataloges of coordinate systems and the EPSG codes you can use for `crs` arguments in `R`:

* [epsg.io](http://epsg.io)
* [Spatial Reference](http://spatialreference.org)

## Common Coordinate Systems
The following are common coordinate systems for mapping in Missouri and, in particular, the St. Louis area. All are based on the NAD 1983 system.

* [Albers Equal Area Conic](http://spatialreference.org/ref/esri/usa-contiguous-albers-equal-area-conic/)
* [Lamber Conformal Conic](http://spatialreference.org/ref/esri/usa-contiguous-lambert-conformal-conic/)
* [NAD 1983](http://spatialreference.org/ref/epsg/nad83/)
* [UTM-15N](http://spatialreference.org/ref/epsg/nad83-utm-zone-15n/)
* [State Plane Missouri East, Feet](http://www.spatialreference.org/ref/esri/102296/)
* [State Plane Missouri East, Meters](http://www.spatialreference.org/ref/esri/102296/)
