# DAA - Competitive Programming (C Implementations)

This repository contains C implementations of classic **Competitive Programming** and algorithmic problems commonly studied in **Design and Analysis of Algorithms (DAA)**.

## 📌 Problem Overview

| # | File Name | Problem Name | Approach / Strategy | Time Complexity | Space Complexity |
|---|---|---|---|---|---|
| 1 | `1-Finding Duplicates-O(n^2) Time Complexity,O(1) Space Complexity` | Finding Duplicate Number | Floyd's Cycle Detection (Tortoise & Hare) | $\mathcal{O}(N)$ | $\mathcal{O}(1)$ |
| 2 | `2-Finding Duplicates-O(n) Time Complexity,O(1) Space Complexity` | Finding Duplicate Number | Floyd's Cycle Detection (Tortoise & Hare) | $\mathcal{O}(N)$ | $\mathcal{O}(1)$ |
| 3 | `4-Print Intersection of 2 sorted arrays-O(m+n)Time Complexity,O(1) Space Complexity` | Intersection of 2 Sorted Arrays | Two-Pointer Linear Scan | $\mathcal{O}(M + N)$ | $\mathcal{O}(1)$ |
| 4 | `5-Pair with Difference-O(n^2)Time Complexity,O(1) Space Complexity` | Pair with Given Difference | Two-Pointer Difference Search | $\mathcal{O}(N)$ | $\mathcal{O}(1)$ |
| 5 | `6-Pair with Difference -O(n) Time Complexity,O(1) Space Complexity` | Pair with Given Difference | Two-Pointer Difference Search (Index Check) | $\mathcal{O}(N)$ | $\mathcal{O}(1)$ |

---

## 📖 Problem Details

### 1 & 2. Finding Duplicate Number (`1-Finding Duplicates...` & `2-Finding Duplicates...`)
- **Objective:** Given an array of $n$ elements where values represent pointers/transitions, detect the duplicate number without extra memory.
- **Approach:** Floyd's Tortoise and Hare cycle detection algorithm:
  - Phase 1: Advance `slow` pointer by 1 step (`a[slow]`) and `fast` pointer by 2 steps (`a[a[fast]]`) until they intersect in a cycle.
  - Phase 2: Reset `slow` to `a[0]` and advance both pointers by 1 step until they meet at the cycle entrance, which indicates the duplicate element.

### 3. Print Intersection of 2 Sorted Arrays (`4-Print Intersection...`)
- **Objective:** Given two sorted arrays $a$ (size $n_1$) and $b$ (size $n_2$), output the common elements present in both arrays.
- **Approach:** Two-pointer technique:
  - If $a[i] == b[j]$, print the element and increment both pointers $i$ and $j$.
  - If $a[i] < b[j]$, increment $i$.
  - Otherwise, increment $j$.

### 4 & 5. Pair with Difference (`5-Pair with Difference...` & `6-Pair with Difference...`)
- **Objective:** Given a sorted array $a$ and an integer $k$, determine if there exists a pair of indices $(i, j)$ such that $a[j] - a[i] == k$.
- **Approach:** Two-pointer traversal initialized at $i = 0, j = 1$:
  - If $a[j] - a[i] == k$ and $i \ne j$, return `1` (true).
  - If the current difference is less than $k$, increment $j$ to increase the difference.
  - If the current difference is greater than $k$, increment $i$ to decrease the difference.
  - If no such pair exists after scanning, output `0`.

---

## 🚀 How to Run

Compile and run any solution using GCC (or Clang):

```bash
# Example: Compile Intersection of Sorted Arrays
gcc "4-Print Intersection of 2 sorted arrays-O(m+n)Time Complexity,O(1) Space Complexity" -o intersection

# Run executable
./intersection
```

---

## 👤 Author
- **Sanjay R** ([@Sanjay-AI-ML](https://github.com/Sanjay-AI-ML))
