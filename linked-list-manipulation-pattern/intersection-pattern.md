# Intersection-Detection Pattern

## Observations

1. [Intersection of two linked List](https://leetcode.com/problems/intersection-of-two-linked-lists/description/) -  Find the intersection point of two given linked list.
2. [Minimum index of two sum lists](https://leetcode.com/problems/minimum-index-sum-of-two-lists/description/) - Find those common words in two lists with its index sum minimum. 

Each questions mentioned above, follows a pattern which tells you to find the first point of two linked list from where there elements are common or one list is a subset of one another.

Keywords to observe before <u style="color: cadetblue">*applying intersection detection pattern*</u> are **inputs in two linked list have some common and you are told to find the intersection point from where the common ones start**.

![alt text](/assets/Intersection_diagram.png)

---

## What Is Intersection-Detection Pattern ?

It is a pattern to find a intersection detection in two open linked list or array from where the elements in the lists are common or to find those elements which are common in both with some condition like minimum sum index of it like above question.

## Approaches.

1. Brute-Force Approach using sets.

```javascript
1. Use a set to store the elements of the first list while iterating over it.
2. Now, iterate over second list from head start.
3. Once, you find the first common element return that.
4. If you don't find any common in the stored set, that means there is no common intersection point return null.
```
2. Better Approach using length calculation and head start with extra step on longer length list.

```javascript
1. Measure the length of two given list.
2. Give the head start up for the longer list by the difference in their length.
3. Now, both are aligned and continue to start the iteration on both list using two pointer as soon as the two pointer points to same element. Return it.
```

3. Optimal Approach (Two pointers with list switching)

```javascript
1. Start with two respective pointers iterating on both list.
2. keep a check on each iteration whether two pointers point to the same element or not. If so, return that element otherwise continue.
3. If both pointers completes its iteration at the same time with no common, return null.
4. If one pointer comes to an end before second pointer, then make that completed pointer to iterate over another list. Same applies on second pointer too.
```
**Note:- Due to so many options, it does not mean that always optimal approach is good, sometimes we need to look for brute force approach as well to handle the scenario. Like in above one of the question to find the minimum index sum, we need to use a hashmap to store the words along with index, so that if the common word are there we can know the minimum sum using their indexes and tell the answer**