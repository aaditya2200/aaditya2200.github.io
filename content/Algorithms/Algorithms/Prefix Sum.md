---
title: "Prefix Sum"
date: 2025-02-02
draft: false
tags:
  - algorithms
---

# What Kind Of Problems?
	1. Sum of ranges.
	2. Ranges with k-sum
	3. Product of all indices except current.
Refer to [resource](https://leetcode.com/discuss/study-guide/5119937/Prefix-Sum-Problems)
for practice problems.

Progress: 
	1. [303. Range Sum Query - Immutable](https://leetcode.com/problems/range-sum-query-immutable/description/). 
	2. [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/description/)
		1. This problem is interesting. We keep track of the frequency of the prefix sums in a map.
	3. [1310. XOR Queries of a Subarray](https://leetcode.com/problems/xor-queries-of-a-subarray/)
		1. This required some thinking, but turns out we can find XOR of a range by taking a prefix array of XORs and computing XOR for the required range indices.
	4. [2559. Count Vowel Strings in Ranges](https://leetcode.com/problems/count-vowel-strings-in-ranges/description/)
		2. This threw me off at first, but after looking at it for a minute, realized it's nothing fancy.
	5. [325. Maximum Size Subarray Sum Equals k](https://leetcode.com/problems/maximum-size-subarray-sum-equals-k/description/)
		1. ** This is a variation of the standard patter. You store index instead of frequency. **
	6. [1248. Count Number of Nice Subarrays](https://leetcode.com/problems/count-number-of-nice-subarrays/description/)
		2. **Fumbled a little bit here. Found two ways to solve this. One is to convert the array into 0 and 1 for even and odd. The other way is to keep track of counts in a map and update when count - k is found.**
