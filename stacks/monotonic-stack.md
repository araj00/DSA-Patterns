# Monotonic Stack Pattern

## Observations

1. [Daily Temperatures](https://leetcode.com/problems/daily-temperatures/description/) - Find the number of days to wait to get warmer temperature days for each given data.
2. [Next Greater Element II](https://leetcode.com/problems/next-greater-element-ii/description/) - Find the next greater element for each data in the input.
3. [Remove K digits](https://leetcode.com/problems/remove-k-digits/description/) - Remove K digits to make the smallest number.
4. [Online stock span](https://leetcode.com/problems/online-stock-span/description/) - Find the span of each given stock during which the stock price was less than or equal to current stock price consecutively in previous days.([This problem can be solved by using design stack pattern also](/stacks/design-stack.md))
5. [Largest rectangle in histogram](https://leetcode.com/problems/largest-rectangle-in-histogram/description/) - Find the largest rectangle that can be found in given histogram.[<sup>3</sup>](#references)

Keywords to observe before <u>*applying monotonic stack pattern*</u> are **find next greater/smaller element or find previous greater/smaller element**.

## What Is Monotonic Stack Pattern ?

A Monotonic stack is a variation of the traditional stack data structure that maintains either a strictly increasing or strictly decreasing order of elements. Unlike a regular stack, where elements can be inserted and removed freely, a monotonic stack enforces a specific order to its elements.

![alt text](/assets/Monotonic_Stack_Pattern.png)

## Approach

```javascript
1. Initialise an empty monotonic stack direction like strict or non-strict depending upon prev or next greater/smaller.
2. Push the indices of the current element maintaining increasing or decreasing stack direction.
3. If any element violates the increasing or decreasing rule then pop that element from that stack and fill the result for the popped index with current element or its index depending upon whatever you were pushing into the stack if it is element then element otherwise index.
4. Iterate over all the elements in the input while maintaining monotonic stack.
5. Return the output.
```

**Notes:-**

```javascript
1. strict vs non-strict - The choice between strict (>) and non-strict (>=) inside the while condition decides what happens to equal elements. With strict comparison, equal elements stay on the stack and become part of the answer chain. With non-strict comparison, equal elements pop each other and are merged.
2. Why store indices instead of values - It keeps positional information available because many problems need the distance between two positions, not just the comparison result. 
```


## References

1. [Hello Interview](https://www.hellointerview.com/learn/code/stack/monotonic-stack)
2. [Algomaster.io](https://algomaster.io/learn/dsa/monotonic-stack-introduction)
3. [Largest Rectangle in histogram](https://www.hellointerview.com/learn/code/stack/largest-rectangle-in-histogram)