# Trapping Rain Water

## 📌 Problem Statement

Given an array of non-negative integers representing the elevation map where the width of each bar is `1`, calculate how much water can be trapped after raining.

### Example

```text
Input:
height = [0, 1, 0, 2, 1, 0, 1, 3, 2, 1, 2, 1]



Output:
6
```

## 💡 Approach

For every position, the amount of trapped water depends on:

* The maximum height on its left
* The maximum height on its right
* The current bar height

The trapped water at a position is:

```text
Water = min(leftMax, rightMax) - height[i]
```

To solve the problem efficiently, the **Two Pointer Approach** can be used.

### Two Pointer Approach

1. Start with two pointers:

   * `left` at the beginning
   * `right` at the end
2. Maintain `leftMax` and `rightMax`.
3. Compare the heights at `left` and `right`.
4. Move the pointer with the smaller height.
5. Calculate trapped water using the corresponding maximum height.
6. Continue until both pointers meet.

## ⏱️ Complexity

| Complexity | Value  |
| ---------- | ------ |
| Time       | `O(n)` |
| Space      | `O(1)` |

## 🧠 Key Concept

The important observation is that water trapped at any position is determined by the **smaller of the maximum heights on both sides**.

Using two pointers allows us to calculate the result in a single traversal without using extra arrays.

## 📂 Repository Contents

```text
Trapping-Rain-Water/
│
├── TrappingRainWater.java
├── Trapping_Rain_Water.pptx
└── README.md
```

## 🎓 Class Presentation

This repository contains the implementation and presentation used for my **Data Structures and Algorithms (DSA)** class presentation on the **Trapping Rain Water** problem.

## 🔗 Problem

**LeetCode:** Trapping Rain Water — Problem #42

## 👨‍💻 Author

**Shubham Dwiwedi**
