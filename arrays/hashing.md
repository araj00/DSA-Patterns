# Hashing Pattern

## Observations

1. [Two Sum](https://leetcode.com/problems/two-sum/description/) - Find the key pair that adds up to a given target value.
2. [Valid Anagram](https://leetcode.com/problems/valid-anagram/description/) - Determine whether the given two string is a valid anagram or not.
3. [Group Anagram](https://leetcode.com/problems/group-anagrams/description/) - Group all the similar anagram under a separate group.
4. [Top K frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/description/) - Find the top K frequent elements.
5. [Happy Number](https://leetcode.com/problems/happy-number/description/) - Find whether the given number is a happy number or not.
6. [Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/description/) - Find whether there is a closed loop in a given linked list or not.
7. [Longest Substring without repeating characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/description/) - Find the longest substring without repeating characters.

Keywords to observe before <u>*applying hashing pattern*</u> is to find if the given question or its solution involves one of the following points:-

1. Find the frequency of each element.
2. If the searching element is already in a given array or not.
3. Finding the duplicate element.
4. Loop or cycle existence in an array or linked list.
5. Finding the unique elements.

**Note:- 

1. Above questions are related to two type of hashing. 1. Storing key-value pairs (A Hashmap)  2. Just storing value as a key (A Set)
2. Some of the questions given above can be solved with other patterns too like finding top K frequent elements using [priority-queue](/heap-and-priority-queue/heap.md) and [fast-pointers (Hare and Tortoise)](/two-pointers-pattern/fast-slow-pointer.md). So, depending upon the question requirement, do the tradeoff.
**

## What Is Hashing Pattern ?

Hashing is a data structure which are used to store the unique elements either as just key or as a key-value pair. This is very helpful in finding the frequencies of unique elements, duplicacy or repetition of the element.

It is very useful in questions where searching of the element requires the time complexity of O(1).

![alt text](/assets/Hashing_Pattern.png)

**Note:- <u>For every questions, there are more than one patterns that can help you to solve your question. So, choose wisely out of that pattern as per the requirement. Think in tradeoff.</u>**