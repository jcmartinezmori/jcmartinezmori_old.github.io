---
layout: page
title: CloudNet Dynamic Pooling of Cloud Resources by Live WAN Migration of Virtual Machines
permalink: /research/cloudnet/
---

# Abstract
Virtualization technology and the ease with which
virtual machines (VMs) can be migrated within the LAN have
changed the scope of resource management from allocating resources
on a single server to manipulating pools of resources
within a data center. We expect WAN migration of virtual machines
to likewise transform the scope of provisioning resources
from a single data center to multiple data centers spread across
the country or around the world. In this paper, we present the
CloudNet architecture consisting of cloud computing platforms
linked with a virtual private network (VPN)-based network infrastructure
to provide seamless and secure connectivity between
enterprise and cloud data center sites. 

To realize our vision of efficiently pooling geographically distributed data center resources,
CloudNet provides optimized support for live WAN migration of
virtual machines. Specifically, we present a set of optimizations
that minimize the cost of transferring storage and virtual machine
memory during migrations over low bandwidth and high-latency
Internet links. We evaluate our system on an operational cloud
platform distributed across the continental US. During simultaneous
migrations of four VMs between data centers in Texas and
Illinois, CloudNet's optimizations reduce memory migration time
by 65% and lower bandwidth consumption for

# Paper
Download [Here](http://mrlucasch.github.io/research/cloudnet/cloudnet.pdf)

{% include embedpaper.html code="cloudnet/cloudnet.pdf" width=100 height=800 %}

# Bibtex

<pre><code>
@article{Wood:2015:CDP:2872492.2872507,
 author = {Wood, Timothy and Ramakrishnan, K. K. and Shenoy, Prashant and Van Der Merwe, Jacobus and Hwang, Jinho and Liu, Guyue and Chaufournier, Lucas},
 title = {CloudNet: Dynamic Pooling of Cloud Resources by Live WAN Migration of Virtual Machines},
 journal = {IEEE/ACM Trans. Netw.},
 issue_date = {October 2015},
 volume = {23},
 number = {5},
 month = oct,
 year = {2015},
 issn = {1063-6692},
 pages = {1568--1583},
 numpages = {16},
 url = {http://dx.doi.org/10.1109/TNET.2014.2343945},
 doi = {10.1109/TNET.2014.2343945},
 acmid = {2872507},
 publisher = {IEEE Press},
 address = {Piscataway, NJ, USA},
 keywords = {cloud computing, virtualization, wide area network (WAN) migration},
} 
</code></pre>

