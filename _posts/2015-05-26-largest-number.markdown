---
layout: post
title:  "[Leetcode] Largest number"
date:   2015-05-26 02:56:00
categories: algorithms
---
>**Question**: Given a list of non negative integers, arrange them such that they form the largest number. For example, given [3, 30, 34, 5, 9], the largest formed number is 9534330. Note: The result may be very large, so you need to return a string instead of an integer.

**Brute force method: Combination**

The first method that probably comes to mind is using combination. Considering the above example of {3, 30, 34, 5, 9}, we can fix 
one number and create combinations of other numbers. This would not only take 2^n time but will probably also run out of memory.

**A little better: Sorting method**

If the numbers were sorted in an order that would give the largest number, our job would be done. But the way it needs to be sorted 
is not numerical, neither is it lexicographical. Let's break down the problem then.

Say for instance there were only 2 elements {30, 34}. To find the largest number here, I would concatenate the strings in the two 
possible ways and compare. So we would compare between 3034 and 3430. 

For 3 elements {30, 34, 9}, going by the same logic,
93034, 93430 and so on....

What we are really doing is concatenating and comparing. Thus we could have a comparator that does just that.

*Special case*

When running through the online judge, it runs test cases with only zeros. This gives outputs with all the zeros in the array. 
Mathematically ofcourse there is no such number. Hence, for this particular case, we need to return just 0.

Below is the source code in JAVA:

<script src="https://gist.github.com/adeydas/ec6cb0a12fb10a099f81.js"></script>
