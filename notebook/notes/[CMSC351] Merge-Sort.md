# Merge Sort

Created: 2023-02-28 11:10:18 -0500

Modified: 2023-02-28 11:34:24 -0500

---

Doing 3 things:

- Merge sorting the left half of the array
  - T(n / 2)
- Merge sorting the right half of the array
  - T(n / 2)
- Merge the two sorted sub-arrays into one sorted array
  - Theta(n)
- T(n) = T(n / 2) + T(n / 2) + cn
- T(n) = 2 * T(n / 2) + cn
  - a = 2
  - b = 2
  - f(n) = cn
  - Log~b~a = log~2~2 = 1
  - f(n) = cn is Θ(n)^1^ -> Case #2
  - T(n) is Θ(nlogn)
- Could also do it using Derivation (Look in notes if you want to see that)

Merge sort is stable, but NOT in place because it requires an auxiliary array

- Best Case, Avg. Case, and Worst Case are all Θ(nlogn)
- Space Utilization = Θ(n) since the most storage that is needed is an additional array of size n at its largest
