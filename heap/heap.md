# Heap Data Structure.

## What Is a Heap ?

Heap is a data structure which helps the programmers to solve the problem related to scheduling or top-K rankings problem like top-K largest element/elements.

Heap is somewhat look like binary search tree but there is a difference as in this, parent node need to be either greater or equal or smaller or equal to its children node depending upon max-heap or min-heap respectively. It is not necessary for children node having to follow some increasing or decreasing order as binary seach tree where left node is either bigger or smaller than right node children.

To learn about heap data structure, we need to learn about 3 things:-

1. How to derive max-heap/min-heap from array of elements.
2. How to do heap-sort.
3. How to create a Priority-Queue.

## 1. How to create max-heap/min-heap from array of elements.

For simplicity, we are going to just have to focus on max-heap example. Below is an illustration on how can we implement max-heap from a given array element.

**Note:- You can maintain either size of length + 1 where 0th index are empty or can have length l starting at 0th index. Choosing either one of it will impact the decision for children node index. If you choose length + 1, then giving parent node index you gonna have children node at (2*i) and (2*i + 1) indices. Otherwise, children node will have (2*i+1) and. (2*i + 2) indices**.

I have chosen the second method, i.e children node will have (2*i+1) and. (2*i + 2) indices.

![alt text](/assets/Max_Heap_Pattern.png)

## 2. How to do heap-sort

1. Take a max-heap/min-heap.
2. Replace the top element of the given heap with last node of the heap. Decrease the size of heap by 1.
3. Apply max-heap/min-heap on root element with new size, decreased by 1 of its previous size.
4. Keep doing it until the new size of heap becomes 1.
5. At the end, you get the elements in sorted form with ascending order, if you choose max-heap.

## 3. How to create a Priority-Queue?

To learn about priority-queue, you should go [this reference](https://www.hackerearth.com/practice/notes/heaps-and-priority-queues/) to learn about priority queue.

## References

1. [Heap](https://www.hackerearth.com/practice/notes/heaps-and-priority-queues/)