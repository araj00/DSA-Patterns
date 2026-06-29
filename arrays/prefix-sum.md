# Prefix Sum Pattern

## Observations

1. [Minimum size subarray sum](https://leetcode.com/problems/minimum-size-subarray-sum/description/) - Find the minimal length of subarray whose sum is greater than or equal to given target.
2. [Product of the last K numbers](https://leetcode.com/problems/product-of-the-last-k-numbers/description/) - Find the product of last K numbers.
3. [Frequency of the most frequent elements](https://leetcode.com/problems/frequency-of-the-most-frequent-element/description/) - Find the maximum possible frequency of an element after performing at most k operations of incrementing each element by 1 to make them most frequent elements.
4. [Split array largest sum](https://leetcode.com/problems/split-array-largest-sum/description/) - Determine how to split the array into K subarrays so that sum of the largest subarray can be minimised.

Points to observe before <u>*applying prefix sum pattern*</u> are:-

1. Question involves some addition or calculation which have associative property. By associative, I mean it is not related to any order no matter how do you group them and do calculation, it will always give you same result. In simple, (a+b+c+d) = (b + c + a + d).
2. Requires you to have a cached result of some calculations like addition or product and reuse them in your next steps easily.

## What Is Prefix Sum Pattern ?

A prefix sum is an array where each element at index i is the sum of all elements from the start up to i in the original array. For example, given nums = [2, 4, 6, 8], the prefix sum array would be [2, 6, 12, 20].

At its heart, prefix sums use the property that sums (and some other operations) are associative the order of grouping doesn’t matter. This allows us to “cache” partial results and reuse them.

![alt text](/assets/Prefix_Sum_Pattern.png)

## Properties

1. Time Complexity: O(N)
2. Space Complexity: O(1) or O(N) depending upon questions like in question calculating sum between two indices it can be O(1) whether to find product of array except self could be O(N)

## References

1. [Prefix Sum Visualization](https://dsaanimator.com/patterns/prefix-sum)