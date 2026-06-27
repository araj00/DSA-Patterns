# K-Way Merge Pattern

## Observations

1. [Find K Pairs With Smallest Sums](https://leetcode.com/problems/find-k-pairs-with-smallest-sums/description/) - Find K pairs with smallest sums.
2. [Kth Smallest Element in a sorted matrix](https://leetcode.com/problems/kth-smallest-element-in-a-sorted-matrix/description/) - Find Kth smallest element in a sorted matrix.
3. [Merge K sorted lists](https://leetcode.com/problems/merge-k-sorted-lists/description/)- .

Keywords to observe before <u>*applying k-way merge pattern*</u> are:-

1. Questions contain two or more arrays or a 2d/3d arrays in a form of matrix.
2. Tells you to find Kth smallest element/elements, pair/pairs or merge the K sorted lists into one single list.

**Note:- If you observe this pattern then it is just an extended version of top-k element pattern with more than one array**

## What Is K-Way Merge Pattern ?

It is a pattern in which a min-heap of size K is maintained to find the smallest element among K sorted lists, if size of heap > K then pop the top element in the heap and add the element from that list where popped element belongs and then maintain a min heap. Keep doing that, until all lists elements are processed.

## Properties

1. Time Complexity:- O(n log K).
2. Space Complexity:- O(K) excluding the space required to give the output if considered then it will become O(n).

## Approach

```javascript
1. Create a min-heap of size K.
2. Add the first elements from K given lists.
3. Find the smallest element through heapify.
4. Pop that element and add a new element from the list where popped element belonged if there is any.
5. Repeat the 3-4 steps until the heap gets emptied after popping up all elements and giving us the final output.
```