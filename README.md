# Trinomial Coefficient Calculator (Brute Force)

A Java implementation for computing trinomial coefficients using recursive brute-force method.

## **Mathematical Definition**

The trinomial coefficient T(n, k) is defined by the recurrence:

1. If n = 0 and k = 0, then T(n, k) = 1
2. If k is outside the range -n to n, then T(n, k) = 0
3. Otherwise: T(n, k) = T(n-1, k-1) + T(n-1, k) + T(n-1, k+1)

## **Usage**

1. **Compile** the program:
   ```bash
   javac TrinomialBrute.java
   ```

2. **Run** with two integer arguments:
   ```bash
   java TrinomialBrute n k
   ```
   - `n`: Power in the expansion (non-negative integer)
   - `k`: Coefficient index (integer)

## **Examples**

```bash
$ java TrinomialBrute 3 3
1

$ java TrinomialBrute 3 0
7

$ java TrinomialBrute 24 12
287134346
```

## **Implementation Details**

- Pure recursive implementation
- Three base cases:
  - T(0,0) = 1
  - T(n,k) = 0 when |k| > n
  - Recursive case sums three previous terms
- Uses `long` to handle large numbers (though limited by recursion depth)

## **Performance Notes**
- Simple but computationally expensive
- Exponential time complexity O(3^n)
- Not practical for n > 30
- Demonstrates need for memoization/dynamic programming

## **Applications**
- Combinatorial mathematics
- Probability calculations
- Analyzing three-outcome experiments
- Card game probability analysis
