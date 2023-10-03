# Binary Trees, Queues, Heaps

Created: 2023-02-28 11:41:45 -0500

Modified: 2023-03-08 18:28:42 -0500

---

In a binary tree, each node has either 0, 1, or 2 children.

Every general tree can be converted to a Binary Tree

Complete Binary Tree: Every level except the last is full, and the last level is filled left to right

Full Binary Tree: Every level is full

Queues:

- Sometimes not everything in the queue is of equal value.
  - This is called a priority queue
  - The things in the queue have a priority level, and we can use a heap to implement a priority queue

Heaps:

- A complete binary tree with an additional property
  - Each node's value is bigger (max heap) or smaller (min heap) than its children's values
  - We will be using max heaps in this class
- We can store this heap in an array
  - Usually we use a 0-indexed array, but in CMSC351, we will use a 1-indexed array because it will make indexing easier In heaps
- If the parent is at index i:
  - Left child index: 2i
  - Right child index: 2i + 1
- If the child is at index j:
  - Parent index: j / 2
- Deleting:
  - We will delete the value at the top of the heap, restore it to a complete binary tree, then "heapify" it to make it a heap again.
    - An example of this whole process is in the slides.
- Heap arrays are sorted in ascending order through level order traversal. (Basis of Heap Sort)
  - How do we construct a Heap from an unsorted array?
    - Trick question, already complete binary tree
- Heap Sort Runtime: Θ(n) in the best case where all the elements are equal, making a CBT is Θ(n) and delete = Θ(1), therefore run time is Θ(n) + Θ(1).
  - Worst case: Θ(nlogn) because making the CBT is Θ(2^d^) where d is the depth of the last level, and removing all the values will take Θ(d * 2^d^) with d = Θ(logn)
- Heap Sort is not stable, but it is in place and the space complexity is Θ(1) since it uses the original array to store the heap
