# Variable-Size Window Pattern

## Observations:-

1. [Contains Duplicate](https://leetcode.com/problems/contains-duplicate-ii/description/) - Find whether there is distinct element or not in a range of [i,j] where abs(i - j) = k.
2. [Minimum operations to reduce to zero](https://leetcode.com/problems/minimum-operations-to-reduce-x-to-zero/description/) - Find the minimum number of operation to reduce a given number to zero by removing just one element at a time either leftmost or rightmost.
3. [Maximum consecutive ones III](https://leetcode.com/problems/max-consecutive-ones-iii/description/) - Return the longest subarray length where you can have consecutive ones after flipping zeros to one at most k times if there are any zeros otherwise just return the array length.

Keywords to observe before <u>*applying variable-size window pattern*</u> is **to achieve a longest subarrays after performing either min or max operations to attain the result like remove/flip the zeros to one to make it longest subarrays</u>**.

## What is Variable-Size Window pattern ?

Variable size window is a sub pattern of sliding window in which two pointers are used to maintain subarrays of size K in an array to solve the problem. This pattern works on previously solved subproblems to reach upto a solution. If you observer, we are just removing and adding a new value in already calculated sum when we shift the start and end pointer to make a new subarrays so that we don't have to work from scratch but pick the problem from the previous checkpoint.

## Approach

1. Initialise two pointers i.e start and end, starting at 0th index.
2. Init variables like sum, avg as per the question and output(result).
3. while end <= arr.length - 1
4. If end - start + 1 <= K, Add the arr[end] value to variables like sum or avg variable.Increment the end pointer.
5. Else, remove the arr[start++] from variables like sum or avg and add arr[++end]
6. Insert the sum value of each subarray to the output at its respective index.
7. End the while.
8. Return the output.

## References

1. [Hello Interview](https://www.hellointerview.com/learn/code/sliding-window/fixed-length)