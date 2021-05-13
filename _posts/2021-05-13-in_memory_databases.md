---
layout: post
title: In-memory Databases
date: 2021-05-13 10:00:18 +1000
categories: tech
---

In-memory databases can be used for enhance your app's performance. They are usually used _in addition_ with disk-based databases. Let's look at a common use case:

# Caching

Let's imagine this use case. The Reddit homepage displays the top 50 most views posts from yesterday. The `Posts` table is not optimized, and each time a user requests this data, the server has to do an expensive query to the database as it requires to do a `full table scan`.
An expensive query means the user has to wait longer.

<div class='container__image'> 
    <img src="{{site.baseurl}}/images/in_memory_databases_1.svg" alt="initial architecture">
    <em>Initial Architecture</em>
</div>

But since we are wizards and know this data set (50 most views posts from yesterday), is heavily requested, we can pro-actively do this expensive query at the beginning of everyday, and duplicate this dataset into the in-memory database. Now each time the server needs this dataset, it can get it from the in-memory database instead.

<div class='container__image'> 
    <img src="{{site.baseurl}}/images/in_memory_databases_2.svg" alt="daily flow architecture">
    <em>Daily flow to update the in-memory database cache</em>
</div>

<div class='container__image'> 
    <img src="{{site.baseurl}}/images/in_memory_databases_3.svg" alt="new architecture">
    <em>New Architecture</em>
</div>

# Benefits

1. The expensive query to the database is now limited to 1 per day (less overload on the database and reducing unnecessary database queries)
2. Each time a user requests this data set, the query is cheap since the data is already sorted, increasing response time
3. Using in-memory instead of disk-based databases are always faster, increasing response time
