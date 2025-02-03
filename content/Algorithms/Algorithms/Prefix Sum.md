---
title: "Prefix Sum"
date: 2025-02-02
draft: false
tags:
  - algorithms
---

# What Kind Of Problems?
1. Sum of ranges.
2. Ranges with k-sum.
3. Product of all indices except current.  

Refer to [resource](https://leetcode.com/discuss/study-guide/5119937/Prefix-Sum-Problems) for practice problems.

## Progress  
4. [303. Range Sum Query - Immutable](https://leetcode.com/problems/range-sum-query-immutable/description/)  
5. [560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/description/)  
   - This problem is interesting. We keep track of the frequency of the prefix sums in a map.  
6. [1310. XOR Queries of a Subarray](https://leetcode.com/problems/xor-queries-of-a-subarray/)  
   - This required some thinking, but turns out we can find XOR of a range by taking a prefix array of XORs and computing XOR for the required range indices.  
7. [2559. Count Vowel Strings in Ranges](https://leetcode.com/problems/count-vowel-strings-in-ranges/description/)  
   - This threw me off at first, but after looking at it for a minute, realized it's nothing fancy.  
8. [325. Maximum Size Subarray Sum Equals k](https://leetcode.com/problems/maximum-size-subarray-sum-equals-k/description/)  
   - **This is a variation of the standard pattern. You store index instead of frequency.**  
9. [1248. Count Number of Nice Subarrays](https://leetcode.com/problems/count-number-of-nice-subarrays/description/)  
   - **Fumbled a little bit here. Found two ways to solve this.**  
     1. Convert the array into 0 and 1 for even and odd.  
     2. Keep track of counts in a map and update when `count - k` is found.  
10. [930. Binary Subarrays With Sum](https://leetcode.com/problems/binary-subarrays-with-sum/description/)  
   - Same as above. However, surprisingly not the fastest in LeetCode.  
11. [2364. Count Number of Bad Pairs](https://leetcode.com/problems/count-number-of-bad-pairs/description/)  
   - Need to revisit. The logic is as follows:  
     1. Total pairs is `n * (n - 1) / 2`.  
     2. For each number in the list, compute `i - nums[i]`.  
     3. Subtract the map value for this index from total pairs.  
     4. Increment map value.  
   - Why does this work? 🤔  
12. [1658. Minimum Operations to Reduce X to Zero](https://leetcode.com/problems/minimum-operations-to-reduce-x-to-zero/)  
   - This was pretty tough to understand, but once I did, it was relatively straightforward.  
