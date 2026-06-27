# Top-K Elements Pattern

## Observations

1. [Kth-Largest Element](https://leetcode.com/problems/kth-largest-element-in-an-array/description/) - Find Kth largest element in an array.
2. [Top K Frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/) - Find the top K frequent elements.
3. [Kth Closest points to origin](https://leetcode.com/problems/k-closest-points-to-origin/description/) - Find the K closest points to origin.

Keywords to observe before <u>*applying top-K elements pattern*</u> is **Find the Kth largest or smallest element**.

## What Is Top-K Elements Pattern ?

Top-K Elements is a pattern in form of heap data structure where we maintain min-heap of K size to find out top K element/elements in an end of the loop.

## Properties

1. Time Complexity:- O(n log K).
2. Space Complexity:- O(K) excluding the space required to give the output if considered then it will become O(n).

## Approach

```javascript
1. Create a min-heap of size K.
2. Keep inserting the elements until size <= K.
3. Once, size > K, pop the root/top of the min-heap and insert a new value while maintaining the min-heap.
4. After processing all elements, return either all elements in a min-heap if it is asking for top-K elements. Or, just return the root of the min-heap to represent top K largest element.
```

## References

1. [Top-K element animation](https://dsaanimator.com/patterns/heap-topk)