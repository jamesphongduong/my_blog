---
layout: post
title: Database Partitioning
date: 2021-04-21 10:00:18 +1000
categories: tech
---

Database partitioning is done to improve maintenance and performance
optimization. There are two ways to partition your database:

1. Vertical Partitioning
2. Horizontal Partitioning

### Horizontal Partitioning

Horizontal partitioning involves _row splitting_ where you choose a _partition
key_ to determine how your data is split. In this example we split the rows
based off the country.

#### Before

#### After

#### Benefits

- Improved query read times due to a smaller sized tables
- Writes to tables won't cause locks other tables

### Vertical Partitioning

- - Writes to tables won't cause locks other tables

#### Before

#### After
