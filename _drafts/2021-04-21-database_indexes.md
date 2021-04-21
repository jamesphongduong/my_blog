---
layout: post
title: Database Indexes
date: 2021-04-21 10:00:18 +1000
categories: tech
---

Database indexes are an optimization technique to improve the speed of database queries. It is the same concept of having a phone book that is sorted alphabetically by the person's name with tabs. If you wanted to look for all the phone records belonging to a John Smith, you would first go to the J tab, and then start your search from there. Now if the phone book was not sorted and had no tabs, doing the same search would require you to look at every individual record from start to finish. This is known as a _full table scan_ (in SQL).

Visualisation

| Horizontal                                               | Vertical                             |
| -------------------------------------------------------- | ------------------------------------ |
| - Load balancer required                                 | - N/A                                |
| - Resilient - load balancer can reroute failing requests | - Single point of failure            |
| - Remote Procedure Calls (slow)                          | - Inter process communication (fast) |
| - Data inconsistency                                     | - Consistent data                    |
| - Scales well                                            | - Hardware limitations               |
| - Cost increases exponentially                           | - Cost increases linearly            |
