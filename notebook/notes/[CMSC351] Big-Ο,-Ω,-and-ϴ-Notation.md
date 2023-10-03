# Big-Ο, Ω, and ϴ Notation

Created: 2023-01-26 11:53:35 -0500

Modified: 2023-01-31 11:36:34 -0500

---

- Recursive method #1 to compute 2^n
  - f(n) = 2^n = 2*2^n-1 = 2* f(n-1)
- Recursive method #2 to compute 2^n
  - f(n) = 2^n = ???

Orders of Magnitude and Big-O Notations

- Running time = T(n)
- N = number of inputs
- Orders of magnitude: n, n^2, n^3, log(n), n*log(n), 2^n
- **T(n) is O(f(n)) iff there exists positive constants, n0 and c, such that:**
  - **T(n) <= c*f(n) for any n >= n0**
    - **f(n) is an upper bound of the growth rate of T(n)**
  - **O(f(n)) is "Big-O**"
- T(n) is O(f(n)) iff there exists positive constants, n0 and c, such that:
  - T(n) <= cf(n) for any n >= n0
  - T(n) is O(n^2)
  - In general, we want the **least upper bound** (As opposed to n^3, n^4, etc.)

Big Omega, Big Theta, Big-O

- Big Omega
  - T(n) is Omega(f(n)) iff there exists positive constants, n0 and c, such that:
    - T(n) >= cf(n) for any n >= n0
    - f(n) is a lower bound of the growth rate of T(n)
- Big Theta
  - T(n) is Theta(f(n)) iff T(n) is O(f(n)) and T(n) is Omega(f(n))
    - f(n) is both an upper and lower bound of the growth rate of T(n)
- Proved that T(n) = 3n^2 + 2n + 1 is O(n^2) above
  - We claim that t(n) is Omega(n^2) and therefore Theta(n^2)
  - T(n) = 3n^2 + 2n + 1 >= 3n^2 for any n >= 0
- We are interested in a tight bound, Big Theta
- In practice, CS industry people talk about Big-Oh and they really mean Big Theta
  - In this class, we will be formal and say Big Theta
- **T(n) = ap n^p + ap-1 n^(p-1) + ... + a1n + a0**
- Intuitively ap n^p is the biggest term
  - Can we find values c of and n0 that work for the above?
    - No, not an explicit value
  - T(n) is <= its absolute value
    - T(n) <= | ap np + ap-1 np-1 + .... + a1 n + a0 |
    - T(n) <= | ap np | + | ap-1 np-1 | + | .... | + | a1 n | + | a0 |
    - For n >= 1 and x >= 0, | n^x | = n^x
    - For n >= 1 and x >= 1, n^x >= n^x-1
      - Thus, T(n) <= | ap | np + | ap-1 | np-1 + ... + | a1 | n^p + | a0 | n^p
      - Factoring by n^p,
        - T( n ) <= n^p ( | ap |+ | ap-1 |+ | .... | + | a1 | + | a0 | )
        - C = | ap |+ | ap-1 |+ | .... | + | a1 | + | a0 |
        - Proved that T(n) = ap n^p + ap-1 n^(p-1) + ... + a1n + a0 is O(n^p)
- To estimate the Big-Theta of a function representing a running time, follow these rules:
  - Keep only the dominant term
  - Ignore the coefficient of the dominant term
  - NOT RIGHT NOW THOUGH, right now you have to prove this.
