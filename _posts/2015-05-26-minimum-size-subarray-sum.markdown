---
layout: post
title:  "Minimum size subarray sum"
date:   2015-05-26 02:56:00
categories: algorithms
---
>**Question**: Given an array of n positive integers and a positive integer s, find the minimal length of a subarray of which the sum ≥ s. If there isn't one, return 0 instead.
>For example, given the array [2,3,1,2,4,3] and s = 7, the subarray [4,3] has the minimal length under the problem constraint.

The logic behind the solution to this problem is as follows:

Take two pointers left and right.

Get a sub-array starting from the initial element that has a sum greater than or equal to the target. If the number of elements in that sub-array is smaller than a previous sub-array, mark the sub-array as a possible solution.

If there are more elements, start from the i+1th element on the left. If the right pointer has reached the end of the original array, there cannot be a smaller sub-array with sum greater than or equal to the target. In that condition, the smallest sub-array so far is the answer.

Below is the source code in JAVA:

<script src="https://gist.github.com/adeydas/29ad1bd8c1a2ca586e79.js"></script>