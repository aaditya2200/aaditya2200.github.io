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
13. [974. Subarray Sums Divisible by K](https://leetcode.com/problems/subarray-sums-divisible-by-k/)
   - This uses the same concept as the basic problem. But, I. need to be careful as to what the question asks for. They didnt ask for subarrays summing to k. They asked for subarrays divisible by k.
   - The formula: `sum = (((sum + item) % k) + k)%k` is important to avoid negative reminders.
14. [1497. Check If Array Pairs Are Divisible by k](https://leetcode.com/problems/check-if-array-pairs-are-divisible-by-k/) 
   - This was tricky. The classic approach does not seem to work for me. What I did, was store all remainders in a map, and then check if all the remainder pairs have the same count. If they dont, the answer is false.
   - If the number of 0 remainders is not even, the answer is false. Why? Well, it's simple. lets say `k = 7`, and we have two number `7` and `21`. If the sum of these 2 numbers is divisible by `k`, the number of zero remainders is even. Tldr, if there exists one number with the remainder 0, the only way that the sum is divisible by 0 is if another number with remainder 0 exists.
15. [1590. Make Sum Divisible by P](https://leetcode.com/problems/make-sum-divisible-by-p/description/)
   - This was tricky. The main idea is as follows:
     - We find the total sum, and check if it is divisible by p. if it is, return 0. 
     - Else, we need to find the subarray which sums up to `total sum % p`
     - Now, we compute prefix sum. For each element, we find `pref % p`.
     - We need to remove the elements from the array, such that the sum of the subarray is divisible by p. The formula for this is `target = (curr - rem + p) % p`.
     - If found in map, update lengths.
16. [523. Continuous Subarray Sum](https://leetcode.com/problems/continuous-subarray-sum/)
   -  I was able to figure this one out. Need to be more careful with respect to if and else condition and updating the map.
17. [2575. Find the Divisibility Array of a String](https://leetcode.com/problems/find-the-divisibility-array-of-a-string/description/)
   - This was easy. But there is a formula I should use: `new_rem = (old_rem * 10 + digit) % m`
18.  [2845. Count of Interesting Subarrays](https://leetcode.com/problems/count-of-interesting-subarrays/description/)
   -  Like 9, first convert to 1 and 0. Then for each num, try to find its complement in the map.
19. [1442. Count Triplets That Can Form Two Arrays of Equal XOR](https://leetcode.com/problems/count-triplets-that-can-form-two-arrays-of-equal-xor/description/)
   - Use this math formula to understand whats going on.
```
prefix[i] .... ^ prefix[j-1] = prefix[j] ^ prefix[i]
prefix[j] ..... prefix[k] = prefix[k + 1] ^ prefix[j]
equating both and eliminating prefix[j]
```





