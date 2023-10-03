# Master Theorem

Created: 2023-02-23 11:01:15 -0500

Modified: 2023-02-23 11:55:38 -0500

---

The Master Theorem applies to recurrence relations where:

- T(n) = a * T(n / b) + f(n)
  - Where a >= 1 and b > 1
  - If b < 1: Problem gets bigger after each recursive call, BAD
  - If b = 1: Problem stays the same size after recursive call, BAD
- Assume f(n) = 0:
  - T(n) = a * T(n / b)
  - Drill down and iterate
  - T(n) = a *(a* (T(n / b^2^))
  - T(n) = a^2^ * T(n / b^2^)
  - T(n) = a^3^ * T(n / b^3^)
  - T(n) = a^k^ * T(n / b^k^)
  - Base Case: n / b^k^ => k = log~b~(n)
  - T(n) = a^log^~b~^n^ * T(1)
  - What is the value of a?
  - n = b^k^
  - Consider c = log~b~a:
    - b^c^ = b^log^~b~^a^ = a
  - a^k^ = (b^c^)^k^ = b^ck^ = b^kc^ = (b^k^)^c^ = n^c^
  - T(n) = n^c^ * T(1), T(n) = Θ(n^c^) where c = log~b~a for f(n) = 0
    - Not very realistic
  - If b = a, then T(n) = Θ(n)
  - If b < a, then c > 1 (worse than Θ(n))
  - If b > a, then c < 1 (better than Θ(n))
  - Ex. b > a: 2 recursive calls but problem size is divided by 3
  - Ex. b > a: Problem size is divided by 2 but 2 recursive calls
- f(n) != 0
