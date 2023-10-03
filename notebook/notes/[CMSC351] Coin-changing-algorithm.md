# Coin changing algorithm

Created: 2023-01-26 11:24:10 -0500

Modified: 2023-01-26 11:43:58 -0500

---

-   Giving change using the least amount of coins (quarters, dimes, nickels, pennies)
-   Solution: Sort the coins in descending order, highest value is "best", lowest value is "worst", choose as many as you can from the best coin, then move down until the value is fulfilled
-   Example of a **Greedy** algorithm
-   Proof:
    -   q + d + n + p = q2 + d2 + n2 + p2
    -   x = 25 * q2 + 10 * d2 + 5 * n2 + p2
    -   0 <= p < 5 (Cannot have 5 or more pennies, could replace with nickel), p = 0, 1, 2, 3 , 4
    -   0 <= n < 2, n = 0, 1
    -   0 <= d < 3, d = 0, 1, 2
    -   Since q2 is the quotient of the division of x by 25, q2 = q (Will be optimal by division)
    -   x - 25 * q = x - 25 * q2 = 10 * d2 + (5 * n2 + p2)
    -   D2 is the quotient of the division of x - 25 * q by 10 -> d2 = d -> n2 = n
    -   The greedy algorithm is optimal for US currency
    -   
