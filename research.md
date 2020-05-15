---
layout: page
title: Research
permalink: /research/
---

## Approximation Algorithms for Special Cases of the Group Steiner Tree Problem [Ongoing]
With Chinmoy Dutta, David Shmoys, and Samitha Samaranayake.

## A Multi-Region SEIR Model with Local Travel [Ongoing, [Website](http://seir.cee.cornell.edu/)]
With collaborators at Cornell, Vanderbilt, and Rutgers Camden.

## pdppy: A Python Library for the Pickup and Delivery Problem [[Library](https://pdppy.readthedocs.io/en/latest/index.html)]
With Adrian Hernandez (undergraduate student).

Adrian's undergraduate research experience was funded by the Louis Stokes Alliance for Minority Participation (LSAMP), administered by [Diversity Programs in Engineering](https://sites.coecis.cornell.edu/lsampreu/) at Cornell University. 

## Bounded Asymmetry in Road Networks [[Paper](https://www.nature.com/articles/s41598-019-48463-z), [Code](https://github.com/jcmartinezmori/bounded_asymmetry_in_road_networks)]
With Samitha Samaranayake.

This research came to be after first getting my feet wet with the metric Traveling Salesman Problem (TSP), which I was interested in because of it's notoriety and numerous natural applications. I spent some time studying its asymmetric variant, namely the ATSP, because TSP-like problems often take place in directed graphs. For instance, road networks contain one-way roads and congestion may depend on the direction of travel. Unfortunately, the known results for the ATSP are much less promising than those for the TSP (more complicated algorithms with worse performance guarantees). It's just a difficult problem!

That said, as far as problems arising in road networks are concerned, it wasn't clear that the ATSP was actually needed in its full generality. For example, in road networks, it doesn't take infinitely longer to go from A to B than it does from B to A. How asymmetric are road networks anyway, and can I pretend that they are symmetric? In this research, I take a look at the (asy)metric space induced by a dozen road networks around the world, and see how far from symmetric they are. The worst case asymmetry ratio between any pair of points in the space is the asymmetry factor of the road network, and if it is bounded by some constant <i>c</i>, it is easy to show that one may solve problems (that aim to minimize the cost of edges picked) on the symmetrized (asy)metric space and only pay an extra factor of <i>c</i> in the algorithm's performance guarantee. The main result is that one is more or less justified in working with the symmetrized (asy)metric space. There's a caveat though: the asymmetry factor <i>c</i> depends on the original distance between the points in the instance (see below).

<p align="center">
  <img src="/images/multiplemaxfactors.png" width="500" />
</p>

In fact, pairs with high asymmetry ratio often look like this! (Source: Map data &copy; 2018 Google)

<p align="center">
  <img src="/images/manhattanuv.png" width="300" />
  <img src="/images/manhattanvu.png" width="300" /> 
</p>

It would be rare that one wants to solve the TSP on every point of a road network. Rather, one typically focuses on a subspace consisting of points of interest. These points typically have non-negligible distance in-between (e.g., the salesman wants to travel around town rather than just going around the corner), justifying the use of algorithms for symmetric instances.

## The Batched Set Cover Problem [[Paper](https://arxiv.org/abs/1811.10767), [Code](https://github.com/jcmartinezmori/the_batched_set_cover_problem)]
With Samitha Samaranayake.

This research started as my final project for Bobby Kleinberg's course. I was interested in modeling an on-demand transit system with 'pop-up' bus stops, similar to what [Via](https://ridewithvia.com/) does, as an online set cover problem. In this application, the potential passenger pickup and dropoff locations are fixed, but they are only brought into the solution as needed by the online arrival of travel requests. Something didn't quite make sense though; travel requests are usually processed in batches rather than one-by-one, precisely to leverage any compatibility between them. Of course, in the worst-case adversarial setting, the adversary reveals batches that mimic the worst-case adversary for the well-studied online setting. To handle this, I instead explored the setting in which the adversary is required to reveal batches of at least a certain VC-dimension. It appears that the structure imposed can be leveraged by primal-dual algorithms to improve their competitive factor by some constant, but I wasn't able to demonstrate this mathematically. Still, I showed a lower bound for any competitive algorithm in this setting, motivated an intuitive primal-dual algorithm with simultaneous dual-variable updates, and explored its performance computationally. The figure below compares the worst-case competitive ratio of a sequential algorithm (left) and an algorithm with simultaneous updates (right) on the instance producing the demonstraded lower bound, as a function of the number of subsets of the ground set <i>m</i> and the VC-dimension requirement <i>z</i>.

<p align="center">
  <img src="/images/alg-b-t.jpg" width="300" />
  <img src="/images/alg-b-d.jpg" width="300" /> 
</p>
