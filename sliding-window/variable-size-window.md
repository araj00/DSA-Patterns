# Variable-Size Window Pattern

## Observations:-

1. [Contains Duplicate](https://leetcode.com/problems/contains-duplicate-ii/description/) - Find whether there is distinct element or not in a range of [i,j] where abs(i - j) = k.
2. [Minimum operations to reduce to zero](https://leetcode.com/problems/minimum-operations-to-reduce-x-to-zero/description/) - Find the minimum number of operation to reduce a given number to zero by removing just one element at a time either leftmost or rightmost.
3. [Maximum consecutive ones III](https://leetcode.com/problems/max-consecutive-ones-iii/description/) - Return the longest subarray length where you can have consecutive ones after flipping zeros to one at most k times if there are any zeros otherwise just return the array length.

Keywords to observe before <u>*applying variable-size window pattern*</u> is **to achieve a longest subarrays after performing either min or max operations to attain the result like remove/flip the zeros to one to make it longest subarrays</u>**.

## What is Variable-Size Window pattern ?

Variable size window is a sub pattern of sliding window in which two pointers are used to maintain subarrays of variable size in an array to solve the problem which involves finding the longest subarrays through operating some operations. 

This pattern works on previously solved subproblems to reach upto a solution. If you observe, we are just operating the operation on previous subarrays to make a new subarray by adjusting previous subarrays through removal or adding.

## Approach

1. Initialise two pointers i.e start and end, starting at 0th index.
2. Init variables like max_subarrays length, operationsDone out of max K operations.
3. while end <= arr.length - 1
4. If operationsDone <= K, increment the length by 1.
5. Else, max(max_subarrays_length, end - start + 1), start++.
6. End the while.
7. Return the max_subarray_length.

## References

1. [Hello Interview](https://www.hellointerview.com/learn/code/sliding-window/variable-length)