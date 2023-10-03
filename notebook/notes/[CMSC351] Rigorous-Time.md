# Rigorous Time

Created: 2023-02-02 12:00:23 -0500

Modified: 2023-02-02 12:10:33 -0500

---

Counting Statements:

-   The addElements method calculates the sum of all elements in an array of size n.
    -   T(n) = 1 + 1 + (n + 1) + n + n + 1 = 1 3n + 4 = Theta(n)
-   The total numbers of statements executed is found by adding the number of time each statement is executed
-   Upper and Lower Bounds
    -   This method determines the maximum value in a two-dimensional array of ints.
    -   To keep it simple, we are assuming that the two-dimensional array is "square", i.e. the number of columns per row is always the same and equal to the number of rows in the array (i.e. we have a n X n two-dimensional array)
    -   T(n) = 1 + ( 2 * n + 2 ) + ( 2 * n2 + 2 * n ) + ( n2 ) + x + 1

= 3 * n2 + 4 * n + 4 + x with 0 <= x <= n * n

-   3 * n2 + 4 * n + 4 <= T(n) <= 3 * n2 + 4 * n + 4 + n2

3 * n2 + 4 * n + 4 <= T(n) <= 4 * n2 + 4 * n + 4

-   T(n) = Theta(n^2)

```{=html}
<!-- -->
```
-   Sequential Search
    -   T(n) = O(n), T(n) = Omega(1)
        -   Consider worst case, best case, and average case run time
        -   In the Average case, we find the element in the middle of the Array, therefore, T(n) = Theta(n)
-   Simple statements are all Theta(1), so we can group them together into c, a time constant
-   Loops take cn + d time, where c and d are constants
