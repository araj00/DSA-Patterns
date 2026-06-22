# Design Stack Design Pattern

## Observations

1. [Min Stack](https://leetcode.com/problems/min-stack/description/) - Design a min stack such that getMin operation can be performed in O(1) time for most of the time.
2. [Online stock span](https://leetcode.com/problems/online-stock-span/description/) - Find the span of each given stock during which the stock price was less than or equal to current stock price consecutively in previous days.
3. [Maximum Frequency Stack](https://leetcode.com/problems/maximum-frequency-stack/description/) - Design a stack such that max frequence elements derivation achieved at O(1) time complexity.

Keywords to observe before <u>*applying design stack pattern*</u> is **to design a stack where you can perform some operation which would feel like performing n times to achieve the output but that should be achieved in O(1) time complexity**.

## What Is Valid Paranthesis Pattern ?

It is a pattern in which stack data structure gets used to transform the O(n) operations into O(1) operations.
![alt text](/assets/Design_Stack_Pattern.png)

## Approach

```javascript
1. Initialise the stack.
2. Perform the push , pop, length function as it is in stack.
3. But, change the push function such that it includes extra data for the operation which are expected to perform in O(1) time complexity rather than O(n) like to get the min element in the stack, max element in the stack etc.
```