---
layout: post
title: Database Indexes
date: 2021-04-26 10:00:18 +1000
categories: tech
---

# ELI5

Imagine if you had a notebook full of lecture notes, and you wanted to organise
your notes alphabetically by the topic so each time you wanted to reference a
topic's notes, you could access it quickly. You could write a reference page at
the back of your book, with alphabetically sorted topics and their corresponding
page numbers.

Your mate sees you do this and thinks you're a genius, and is inspired to
reorganise his own notes. However, his notes are on a laptop - so he decides
instead of creating a reference page, to just rearrange the notes alphabetically
by topic.

With both of these techniques, we are able to able to navigate to a topic much
faster and this was made possible by having sorted data, the key ingredient to
database indexes.

# Technical Explanation

Database indexes are a _sorted_ data structure and optimisation techique used to
improve the speed of database queries at the cost of slower data writes. With
database indexes, we are able to query data in _logarithmic_ time, as opposed to
_linear_ time.

# Clustered Indexes and Non-Clustered Indexes

Non-Clustered Index: Makes a copy of the indexed column and uses a lookup to the
actual data. Requires additional writes and storage space. (notebook example)

Clustered Indexes: The data itself is sorted when stored (which means there can
only be one clustered index). Does not require additional storage space. (laptop
example)

# Types of Scans

1. Sequential Scan: Scans entire table - slow
2. Index Scan: Scans rows within index, then lookups in heap
3. Index-only Scan: Scans all/some rows in index only (no further lookup
   required)
4. Bitmap Heap Scan: Scans index to build bitmaps for pages (for AND / OR
   queries), then looks up relevant pages

# Best Practices

- Create indexes on highly selected columns
- Be aware of implications of updates & deletes on indexed columns - these are
  more expensive!
- Don't over-optimise early as indexes are expensive
