---
layout: post
title: Binary Search
date: 2021-04-21 10:00:18 +1000
categories: tech
---

A binary search is a search algorithm used to find the position of a target
value in a _sorted_ list and has a Big O Notation of `O(log n)`. The algorithm
repetitively halves the list until the target value is acquired.

# Example

Let's imagine we are looking at a sorted list of 8 numbers and we are looking
for the number 7. (worse case scenario in terms of effort required)

We first half the list, and compare the numbers beside them with the target
number. If the left number is less than the target number, we know that the
target number will exist in the left half, and so we can discard the right half.
Then we repeat the process until we find our number.

![binary search diagram](/images/binary_search.svg)

We are able to split our list of _8_ numbers a total of _3_ times until we are
able to find our target value of 7. We can see our Big O Notation formula
corresponds with this.

`log base 2 of 8 = 3`
