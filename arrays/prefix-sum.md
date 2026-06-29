# Prefix Sum Pattern

## Observations

1. [Minimum size subarray sum](https://leetcode.com/problems/minimum-size-subarray-sum/description/) - Find the minimal length of subarray whose sum is greater than or equal to given target.
2. [Product of the last K numbers](https://leetcode.com/problems/product-of-the-last-k-numbers/description/) - Find the product of last K numbers.
3. [Frequency of the most frequent elements](https://leetcode.com/problems/frequency-of-the-most-frequent-element/description/) - Find the maximum possible frequency of an element after performing at most k operations of incrementing each element by 1 to make them most frequent elements.
4. [Split array largest sum](https://leetcode.com/problems/split-array-largest-sum/description/) - Determine how to split the array into K subarrays so that sum of the largest subarray can be minimised.

points to observe before <u>*applying prefix sum pattern*</u> are:-

1. Question should contain the elements in the given range [1, n] or [0, n].
2. Requires you to find the duplicate or missing numbers.

## What Is Cyclic Sort Pattern ?

Cyclic sort is an in-place, unstable-sorting algorithm. It transforms input without using any other auxiliary data structure. As the algorithm executes the input is overwritten by the output. Unstable algorithm doesn't preserve the relative order of equal elements while sorting.

![alt text](/assets/Cyclic_Sort_Pattern.png)

## Properties

1. Time Complexity: O(N)
2. Space Complexity: O(1)

## References

1. [Cyclic Sort](https://leetcodethehardway.com/tutorials/basic-topics/sorting/cyclic-sort)
2. [Questions explaination](https://www.youtube.com/watch?v=JfinxytTYFQ)