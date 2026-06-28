# Merge Sorted Array Pattern

## Observations

1. [Square of a sorted array](https://leetcode.com/problems/squares-of-a-sorted-array/description/) - Make the sorted array into a square of a sorted array.
2. [Merge two sorted arrays](https://leetcode.com/problems/merge-sorted-array/description/) - Merge two sorted arrays into one sorted array.

Keywords to observe before <u>*applying merge sorted array pattern*</u> is **"if question requires no use of extra space to merge two sorted arrays into one.**

## What Is Merge Sorted Array Pattern ?

It is a pattern of array which uses pointer on each array, starting from its end, to evaluate the current greater values from two sorted arrays to make a merge sorted array.

![alt text](/assets/Merge_Sorted_Array_Pattern.png)

## Approach

```javascript
1. Initialize three pointers:
    i. i at the last valid element of nums1 (i.e., m - 1)
   ii. at the last element of nums2 (i.e., n - 1)
  iii. k at the very end of nums1 (i.e., m + n - 1)
2. Compare and Place:
    i. At each step, compare nums1[i] and nums2[j].
   ii. Place the larger value at nums1[k].
  iii. Move the corresponding pointer(s) backward.
3. Finish Up:
    i. If nums2 still has elements left, copy them into nums1.
   ii. If nums1 has elements left, they’re already in place.
```

## Properties

1. Time Complexity: O(m+n).
2. Space Complexity: O(1).