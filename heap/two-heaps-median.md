# Two Heaps Median Pattern

## Observations

1. [Finding median from data stream](https://leetcode.com/problems/find-median-from-data-stream/description/) - Find K pairs with smallest sums.

Keywords to observe before <u>*applying two-heaps median pattern*</u> is "find the median of a given array/list"

## What Is Two-Heaps Median Pattern ?

It is a pattern in which two heaps are used to create a min-heap and max-heap. Min-heap is used to store the upper half of values in a given array while max-heap is used to store the lower half of values.

**Note:-**

<u>*If you ask why is it like that? That is because, Median will always either be one medium value if n is odd or two medium values if n is even. Medium Values always contain the highest value of lower half and/or lowest value of upper half. That is why, min-heap is used to give the lowest value of upper half after the completion whether max-heap to give highest value of upper lower half.*<u>

## Properties

1. Time Complexity:- O(n log n).
2. Space Complexity:- O(n) including max-heap and min-heap.

## Approach

```javascript
1. Create two heaps:- one min-heap and another max-heap.
2. Always add value to max-heap. Keeping the difference in their(two-heaps) size to be <= 1
3. Balance Rule:- 
    1. If min-heap size > max-heap size then transfer the top from min-heap to max-heap.
    2. If min-heap top value < max-heap top value then exchange the top values of both heaps with each other.
    3. If difference in heaps size > 1; then try to balance it or bring the difference to 1.
4. Keep repeating 2-3 steps until all values are processed.
5. Calculate the median based on total size of min and max heap. If it is odd, then return top of max-heap else return sum of top values of max and min heap divided by 2.
```

## References

1. [Two-Heaps median animation](https://dsaanimator.com/patterns/heap-two-heaps)