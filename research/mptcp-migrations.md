---
layout: page
title: Fast Transparent Virtual Machine Migration in Distributed Edge Clouds
permalink: /research/mptcp-migrations
---

# Abstract
Edge clouds are emerging as a popular paradigm of computation.
In edge clouds, computation and storage can be
distributed across a large number of locations, allowing applications
to be hosted at the edge of the network close to
the end-users. Virtual machine live migration is a key mechanism
which enables applications to be nimble and nomadic
as they respond to changing user locations and workload.
However, VM live migration in edge clouds poses a number
of challenges. Migrating VMs between geographically
separate locations over slow wide-area network links results
in large migration times and high unavailability of the application.
This is due to network reconfiguration delays as
user traffic is redirected to the newly migrated location. In
this paper, we propose the use of multi-path TCP to both
improve VM migration time and network transparency of
applications.
We evaluate our approach in a commercial public cloud
environment and an emulated lab based edge cloud testbed
using a variety of network conditions and show that our approach
can reduce migration times by up to 2X while virtually
eliminating downtimes for most applications.

# Paper
Download [Here](http://mrlucasch.github.io/research/sec17/sec17.pdf)

{% include embedpaper.html code="sec17/middleware16.pdf" width=100 height=800 %}

# Slides

Download [Here](http://mrlucasch.github.io/research/sec17/sec17_slides.pdf)

{% include embedpaper.html code="sec17/mw.pdf" width=100 height=500 %}

# Bibtex

<pre><code>
TBD
</code></pre>

