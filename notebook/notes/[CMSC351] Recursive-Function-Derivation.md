# Recursive Function Derivation

Created: 2023-02-21 14:22:55 -0500

Modified: 2023-02-23 11:59:42 -0500

---

Runtime of a Recursive Function:

-   Factorial:
    -   T(n) = T(n - 1) + c => T(x) = T(x - 1) + c
    -   T(n - 1) = T(n - 2) + c
    -   T(n) = (T(n - 2) + c) + c
    -   T(n) = T(n - 2) + 2c
    -   T(n) = T(n - k) + kc
    -   Base Case: n - k = 0 or k = n
    -   T(n) = T(0) + cn
    -   cn + d = Θ(n)
-   MCS Divide and Conquer:
    -   T(n) = c1 + c2 + T(n / 2) + T(n / 2) + Θ(n) + c3 (Look back at MCS if you don't understand where this comes from)
    -   T(n) = 2 * T(n / 2) + Θ(n) + c1 + c2 + c3
    -   T(n) = 2 * T(n / 2) + Θ(n) + c // c = c1 + c2 + c3
    -   T(n) = 2 * T(n / 2) + Θ(n) = 2 * T(n / 2) + cn
    -   T(n / 2) = 2 * T(n / 2^2^) + c(n / 2)
    -   T(n) = 2 * (2 * T(n / 2^2^) + c(n / 2)) + cn => 2^2^ * T(n / 2^2^) + 2cn
    -   T(n) = 2^k^ * T(n / 2^k^) + kcn
    -   Base Case: n / 2^k^ = 1 or n = 2^k^ => log(n) = log(2^k^) = k * log(2) = k
    -   T(n) = n * T(1) + cnlog(n)
    -   T(n) = Θ(nlog(n))
-   Recursive Binary Search:
    -   T(n) = a (first if) + b (second if) + T(n / 2) (because only one side will actually be chosen) = c + T(n / 2)
    -   T(n / 2) = (T(n / 2^2^) + c) + c
    -   T(n) = T(n / 2^2^) + 2c
    -   T(n) = T(n / 2^k^) + kc
    -   Base Case: n / 2^k^ = 1 => n = 2^k^ => k = log(n) = log(2^k^) = k * log(2) = k
    -   T(n) = T(1) + clog(n) = Θ(log(n))
-   Fibonacci (Faster with Recursive than Loop, unlike Binary Search, which is the same)
-   Powers of 2A:
    -   T(n) + T(n - 1) + T(n - 1) + c
    -   T(n) = 2 * T(n - 1) + c
    -   T(n) = 2 * (2 * T(n - 2) + c) + c
    -   T(n) = 2^2^ * T(n - 2) + 2c + c
    -   T(n) = 2^3^ * T(n - 3) + 2^2^c + 2c + c
    -   T(n) = 2^k^ * T(n - k) + c(2^k-1^ + 2^k-2^ + ... + 2 + 1)
    -   T(n) = 2^k^ * T(n - k) + c(2^k^ - 1)
    -   Base Case: n - k = 0 or n = k
    -   T(n) = 2^n^ * T(0) + c(2^n^ - 1) = Θ(2^n^)



