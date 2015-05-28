---
layout: post
title:  "[Leetcode] Isomorphic Strings"
date:   2015-05-28 15:30:00
categories: algorithms
---
>**Question**: Given two strings s and t, determine if they are isomorphic.

>Two strings are isomorphic if the characters in s can be replaced to get t.

>All occurrences of a character must be replaced with another character while preserving the order of characters. No two characters may map to the same character but a character may map to itself.

>For example,
>Given "egg", "add", return true.

>Given "foo", "bar", return false.

>Given "paper", "title", return true.

>Note:
>You may assume both s and t have the same length.

Two strings are isomorphic if the characters from the first string and characters from the second string map to each other aka they hold 
a bijection property.

So, the algorithm could be as simple as checking individually from both sides, giving it a time complexity of O(n+n) = O(n).

<script src="https://gist.github.com/adeydas/5a710c5bd8273110e234.js"></script>
