# Quick Sort

Created: 2023-03-07 11:02:33 -0500

Modified: 2023-03-07 12:07:54 -0500

---

Like merge sort, divide and conquer

Idea: Separate the array into 2 p arts before making the recursive calls on both parts

-   Left: Smaller element
-   Right: Larger elements



Process:

1.  Pick one element ("pivot"), and partition elements such that

    a.  Left: elements will be smaller than or equal to the pivot

    b.  Right: elements will be larger than pivot

2.  We can pick whatever element to be the pivot (We will use the last)
3.  Now, the pivot is in the correct position, but the left and right sides are unsorted.
4.  Run quick sort on the left and right sides until they are size 1 or size 0.



Partition:

1.  For each partition, go through the array and keep track of the leftmost element that is larger than the pivot.
2.  Whenever we encounter a value that is smaller than the pivot, swap it with the index we have saved and increment the index by 1 (Doesn't matter what the value of that element is since it is guaranteed to be greater than the pivot)
3.  (Example is on Canvas, very good visualization)



Runtimes on the slides: [Files (instructure.com)](https://umd.instructure.com/courses/1338797/files/folder/Ppt%20Slides/week7%3A%20Quicksort%2C%20Limits%20on%20comparison%20sorting?preview=72273778)

Quick Sort is in-place, but not stable



Average Case: [Files (instructure.com)](https://umd.instructure.com/courses/1338797/files/folder/Ppt%20Slides/week7%3A%20Quicksort%2C%20Limits%20on%20comparison%20sorting?preview=72274288)
