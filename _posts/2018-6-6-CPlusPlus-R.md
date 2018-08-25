---
layout: post
title: Recommendation System in C++ using GPUs!
---
I did a group project with Alister Johnson implementing a recommendation system using cuBlas! We ran this on the HPC Talapas at the University of Oregon. To sum up most of our issues - memory management. When allocating and using variables it is important to understand what is accessing what, and at what time. 
github link [repo](https://github.com/ajohnson-uoregon/CIS631-team-project) 