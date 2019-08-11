---
layout: page
title: Research
permalink: /research/
---

## The Group Traveling Salesman Problem [Ongoing]
With Chinmoy Dutta, David Shmoys, and Samitha Samaranayake.

## Approximation Algorithms and Heuristics for the Pickup and Delivery Problem [Ongoing]
With Adrian Hernandez and Samitha Samaranayake.



## Bounded Asymmetry in Road Networks [Link]
With Samitha Samaranayake.

## The Batched Set Cover Problem [[Link](https://arxiv.org/abs/1811.10767)]
With Samitha Samaranayake.

This research started as my final project for Bobby Kleinberg's course. I was interested in modeling an on-demand transit system with 'pop-up' bus stops, similar to what [Via](https://ridewithvia.com/) does, as an online set cover problem. In this application, the potential passenger pickup and dropoff locations are fixed, but they are only brought into the solution as needed by the online arrival of travel requests. Something didn't quite make sense though; travel requests are usually processed in batches rather than one-by-one, precisely to leverage any compatibility between them. Of course, in the worst-case adversarial setting, the adversary reveals batches that mimic the worst-case adversary for the well-studied online setting. To handle this, I instead explored the setting in which the adversary is required to reveal batches of at least a certain VC-dimension. It appears that the structure imposed can be leveraged by primal-dual algorithms to improve their competitive factor by some constant, but I wasn't able to demonstrate this mathematically. Still, I showed a lower bound for any competitive algorithm in this setting, motivated an intuitive primal-dual algorithm with simultaneous dual-variable updates, and explored its performance computationally. The figure below compares the worst-case competitive ratio of a sequential algorithm (left) and an algorithm with simultaneous updates (right) on the instance producing the demonstraded lower bound, as a function of the number of subsets of the ground set <i>m</i> and the VC-dimension requirement <i>z</i>.

<p align="center">
  <img src="/images/alg-b-t.jpg" width="300" />
  <img src="/images/alg-b-d.jpg" width="300" /> 
</p>
