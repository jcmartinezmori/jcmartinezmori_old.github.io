---
layout: page
title: Research
permalink: /research/
---

## The Group Traveling Salesman Problem [Ongoing]
With Chinmoy Dutta, David Shmoys, and Samitha Samaranayake.

## Bounded Asymmetry in Road Networks [Link]
With Samitha Samaranayake.

## The Batched Set Cover Problem [[Link](https://arxiv.org/abs/1811.10767)]
With Samitha Samaranayake.

This research started as my final project for Bobby Kleinberg's course. I was interested in modeling an on-demand transit system with 'pop-up' bus stops, similar to what [Via](https://ridewithvia.com/) does, as an online set cover problem. In this application, the potential passenger pickup and dropoff locations are fixed, but they are only brought into the solution as travel requests arrive. Something didn't quite make sense though; travel requests are usually processed in batches rather than one-by-one, precisely to leverage compatibility between distinct travel requests. Of course, in the worst-case, the adversary reveals batches that mimic the worst-case online setting. To handle this, I instead explored a setting in which the adversary is required to reveal batches that have a minimum VC-dimension requirement. 
