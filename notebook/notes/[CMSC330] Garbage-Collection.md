# Garbage Collection

Created: 2023-04-13 12:35:56 -0400

Modified: 2023-04-13 13:33:24 -0400

---

Manual Memory Mgmt.

-   Like in C

Automatic Memory Mgmt.

-   Like in Java
    -   Garbage Collector: Go through memory and free things we don't need



Garbage Collector:

-   Is theoretically less efficient than manual
-   Works behind the scenes (programmer doesn't need to deal with it)
-   Traverses heap



3 diff kinds of memory mgmt.:

-   Reference counting
    -   If reference to a piece of data is 0, free it.
    -   Negatives: Can create memory leaks with circular references
-   Mark & sweep algorithm
    -   Go through stack, check if memory is accessible, if not, free it.
    -   Negatives: Prone to fragmentation, need to stop program
-   Stop & copy algorithm
    -   Stop program, copy all live data to the off section, swap partitions (halves of heap)
    -   Negatives: Need to stop program, copy a lot of data, can only use half the heap
