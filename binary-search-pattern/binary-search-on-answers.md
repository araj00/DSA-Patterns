# Binary Search On Answer Pattern

## Observations

1. [Koko eating bananas](https://leetcode.com/problems/koko-eating-bananas/description/) - Find the minimum speed k at what koko can eat all given bananas in the input within given hour.
2. [Maximum candies allocated to children](https://leetcode.com/problems/maximum-candies-allocated-to-k-children/description/) - Find the maximum candies which can be distributed among K children equally from the given piles of candies and make sure that each child can be allocated candies from only one pile of candies and some piles of candies may go unused.

In above questions, it can be seen to find the minimum or maximum ways to find the output.

Keywords to observe before <u>*applying binary search on answer pattern*</u> in **find the minimum/maximum ways which given input can be ingested efficiently**.

## What Is Binary Search Pattern ?

It is a pattern in which binary search is used on all possible answers from lowest answer to highest answer to find the minimum/maximum answer.

## Approaches

Binary Search Approach

```javascript
1. Find the low and high value to create a range in which you will search based on the question.
2. Take the mid value using low and high value, and check whether that satisfies the required condition or not.
3. If it satisfies, store that value in the variable, and change the low or high value based on the objective to find max or min in question respectively.
4. Once, you have completed the binary search
5. Return the output.
```

Note:- "There is an iterative approach in which you check every values of the range leading to O(n * O(number of values in range)) time complexity, while binary search gives O(n * (log(num of values in range)))

Some Advanced patterns based on binary search:-

[Median of two sorted arrays](https://ritvik-blog.vercel.app/posts/35-leetcode-median-of-two-sorted-arrays)
[Kth element of sorted array](https://dsa-explorer-hub.vercel.app/algorithm/quick-select) - It is related to quick select algorithm