---
layout: page
title: Containers and Virtual Machines at Scale A Comparative Study
permalink: /research/containers-vms/
---

# Abstract
Virtualization is used in data center and cloud environments to decouple
applications from the hardware they run on. Hardware virtualization
and operating system level virtualization are two prominent
technologies that enable this. Containers, which use OS virtualization,
have recently surged in interest and deployment. In this
paper, we study the differences between the two virtualization technologies.
We compare containers and virtual machines in large data
center environments along the dimensions of performance, manageability
and software development.

We evaluate the performance differences caused by the different
virtualization technologies in data center environments where multiple
applications are running on the same servers (multi-tenancy).
Our results show that co-located applications can cause performance
interference, and the degree of interference is higher in the case of
containers for certain types of workloads. We also evaluate differences
in the management frameworks which control deployment
and orchestration of containers and VMs. We show how the different
capabilities exposed by the two virtualization technologies can
affect the management and development of applications. Lastly, we
evaluate novel approaches which combine hardware and OS virtualization.

# Paper
Download [Here](http://itsalgorithmic.com/papers/middleware16/middleware16.pdf)

{% include embedpaper.html code="middleware16/middleware16.pdf" width=100 height=800 %}

# Slides

Download [Here](http://mrlucasch.github.io/research/middleware16/mw.pdf)

{% include embedpaper.html code="middleware16/mw.pdf" width=100 height=500 %}

# Bibtex

<pre><code>
@inproceedings{Sharma:2016:CVM:2988336.2988337,
 author = {Sharma, Prateek and Chaufournier, Lucas and Shenoy, Prashant and Tay, Y. C.},
 title = {Containers and Virtual Machines at Scale: A Comparative Study},
 booktitle = {Proceedings of the 17th International Middleware Conference},
 series = {Middleware '16},
 year = {2016},
 isbn = {978-1-4503-4300-8},
 location = {Trento, Italy},
 pages = {1:1--1:13},
 articleno = {1},
 numpages = {13},
 url = {http://doi.acm.org/10.1145/2988336.2988337},
 doi = {10.1145/2988336.2988337},
 acmid = {2988337},
 publisher = {ACM},
 address = {New York, NY, USA},
} 
</code></pre>

