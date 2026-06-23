# Fixed-Size Window Pattern

## Observations:-

1. [Find X sum of all k long subarrays 1](https://leetcode.com/problems/find-x-sum-of-all-k-long-subarrays-i/description/) - Find the sum of top X frequent elements in all K long subarrays.
2. [Find the power of all K size subarrays](https://leetcode.com/problems/find-the-power-of-k-size-subarrays-i/description/) - Find the power of all K size subarrays.

Keywords to observe before <u>*applying fixed-size window pattern*</u> is **to find sum, average, of all <u>K contiguous subarray</u>**.

## What is Fixed-Size Window pattern?

Fixed size window is a sub pattern of sliding window in which two pointers are used to maintain subarrays of size K in an array to solve the problem which involve working on all K size subarrays. 

This pattern works on previously solved subproblems to reach upto a solution. If you observe, we are just removing and adding a new value in already calculated sum when we shift the start and end pointer to make a new subarrays so that we don't have to work from scratch but pick the problem from the previous checkpoint.

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