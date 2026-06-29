# Binary Search Pattern

## Observations

1. [Search a 2D matrix](https://leetcode.com/problems/search-a-2d-matrix/description/) - Find whether the given target is in 2D matrix or not, given the first element in the ith row is greater than last element in previous row.
2. [Single element in a sorted array](https://leetcode.com/problems/single-element-in-a-sorted-array/description/) - Find the single element in a sorted array.

Points to observe before <u>*applying binary-search pattern*</u> are **find the given element, find the first and last occurence of the element, or find the missing value or special value, in a sorted array**.

## What Is Binary Search Pattern ?

It is to use two pointers to maintain the low and high value of the sorted list to find an element in O(log n) rather than O(n).

![alt text](/assets/Binary_Search_Pattern.png)

## Approaches

1. Iterative approach

```javascript
1. Iterate over each element one by one.
2. If the existing element == target element.
3. Return true or false.
```

2. Binary Search Approach

```javascript
1. Start with two pointers: left at 0, right at the end of the array.
2. While left <= right, find the mid index.
3. If nums[mid] is the target, return mid.
4. If nums[mid] is less than the target, move left to mid + 1.
5. If nums[mid] is greater, move right to mid - 1.
6. If the loop ends without finding the target, left will be at the position where the target should be inserted.
```