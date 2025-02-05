---
title: "Tries"
date: 2025-02-04
draft: false
tags:
   - algorithms
   - tries
---
## Tries
**When to use?**
1. To find common prefixes.
2. To verify existence of words within a set of strings

**In real world systems, tries are used in autocomplete**.

## Types of problems
1. Implementation of trie
2. Wildcard search
3. Find all words on a board

**Please use this [resource](https://leetcode.com/discuss/general-discussion/853098/trie-or-search-related-question-and-good-explanation) for practice.**
### Problems
1. [Trie Implementation](https://leetcode.com/problems/implement-trie-prefix-tree)
   - Use a map to store pointers from ch to TrieNode
   - **Improvement**: use a `TrieNode*` array of 26 length. Access each char by subtracting `a` from it.
2. [Wildcard Search](https://leetcode.com/problems/design-add-and-search-words-data-structure/)
   - Be careful. The base case for recursion should be when `index == word.size()` this is because when you start at root, index is 0, and you are searching the next level for character 0. Meaning, for each index, you are searching the next level, and not the current level. That is why the standard string condition of `size - 1` fails. Remember that the root is essentially a dummy node.
3. [Word Search 2](https://leetcode.com/problems/word-search-ii/)
   - This is a bit tricky. The idea is simple, but the implementation is tricky
4. [Prefix Suffix Search](https://leetcode.com/problems/prefix-and-suffix-search/)
   - Straightforward. Insert all prefixes and suffixed. For example, for `apple`, we insert `a#apple, ap#apple, ... apple#apple, #apple, e#apple, le#apple` etc.
   - Maintain index of the word as you encounter them. `apple` would have index 0.
   - Maybe dont even need prefix