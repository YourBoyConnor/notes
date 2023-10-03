# Arithmetic and Geometric Review

Created: 2023-01-31 11:36:35 -0500

Modified: 2023-02-07 11:56:45 -0500

---

Arithmetic and Geometric Series

- **Arithmetic Series: For n >= 1, S(n) = 1 + 2 + ... + (n-1) + n = n(n + 1) / 2**
- Prove by induction
  - Step 1: Check that the formula is correct for base case(s), i.e. n = 1
  - Step 2 (Inductive step): Assuming the formula is correct for n, prove that it is correct for n + 1
    - True for Step 1
    - S(n + 1) = 1 + 2 + ... + (n + 1) + n + (n + 1)
      - Is this equal to (n + 1)(n + 2) / 2 ?
      - S(n + 1) = S(n) + (n + 1)
      - S(n + 1) = n(n + 1) / 2 + (n + 1)
      - S(n + 1) = (n + 1)(n/2 + 1) = (n + 1)(n/2 + 2/2) = (n + 1(n + 2)/2
      - Done
- Proof not using induction
  - Write S(n) left to right and right to left
    - S(n) = 1 + 2 + ... + (n-1) + n
    - S(n) = n + (n-1) + ... + 2 + 1
    - What does each pair have in common?
      - Sum of each pair is n + 1
      - S(n) + S(n) = (n + 1) + (n + 1) + ... + (n + 1) + (n + 1)
      - N terms
        - Thus, 2 S(n) = n(n + 1)
        - S(n) = n(n + 1) / 2
- **Geometric Series: For n >= 1, G(n) = 1 + a + a^2 + ... + a^(n-1) + a^n = (a^(n+1) - 1) / (a - 1) for a != 1**
  - For a = 1, G(n) = n, we will assume that a != 1
  - Step 1: Check that the formula is correct for base cases(s), i.e. n = 1
    - Is 1 + a = (a^(1 + 1) - 1) / (a - 1) = (a^2 - 1) / (a - 1)? Yes
    - Done with Step 1
  - Step 2 (Inductive step): Assuming the formula is correct for n, prove that it is correct for n + 1
    - G(n + 1) = 1 + a + a^2 + ... + a^(n - 1) + a^n + a^(n + 1) ?= (a^(n + 1) - 1) / (a - 1)

- Proof not involving induction:
  - Multiply by a left and right
  - G(n) = 1 + a + a^2 + ... + a^(n-1) + a^n
  - aG(n) = a + a^2 + ... + a^n + a^(n + 1)
    - aG(n) = G(n) = a^(n + 1) - 1

G(n = (a^(n + 1) - 1) / (a - 1) for a != 1

- T(n) = 1 + 2 + 3 + ... + n-1 + n
- T(n) <= n + n + n + ... + n + n = n^2
- T(a) >= (a/2) + ... + (a-1) + a
- T(a) >= (a/2) + ... + (a/2) + (a/2)
- T(a) >= (a^2) / 4
- T(a) = au^2 + bn + c
  - Since T(0) = 0 -> c = 0
  - T(1) = 1 = a + b
  - T(a) = an^2 + bn
  - T(n + 1) = T(n) + (n + 1) = an^2 + bn + n + 1
    - a(n + 1)^2 + b(n + 1)
    - = a(n^2 + 2n + 1) + b(n + 1)
    - = an^2 + (2a + b)n + (a+b)
