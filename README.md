# 🔍 Search in Rotated Sorted Array (LeetCode 33)

[![Java](https://img.shields.io/badge/Language-Java-orange.svg)](https://www.java.com)
[![Difficulty](https://img.shields.io/badge/Difficulty-Medium-yellow.svg)](https://leetcode.com/problems/search-in-rotated-sorted-array/)
[![Status](https://img.shields.io/badge/Status-Solved-success.svg)]()

A robust, high-performance **Java** implementation for solving the classic **Search in Rotated Sorted Array** problem in **$O(\log n)$** time complexity.

---

## 📋 Problem Statement

There is an integer array `nums` sorted in ascending order (with distinct values). Prior to being passed to your function, `nums` is possibly left-rotated at an unknown index `k` ($1 \le k < \text{nums.length}$).

Given the array `nums` after the possible rotation and an integer `target`, return the index of `target` if it is in `nums`, or `-1` if it is not in `nums`.

You must write an algorithm with **$O(\log n)$** runtime complexity.

---

## 💡 Approach & Intuition

Even though the array has been rotated, dividing it in half will **always result in at least one strictly sorted half**. 

1. Find the middle element (`mid`).
2. Determine which half of the array (left or right) is normally sorted.
3. Check if the `target` falls within the boundaries of the sorted half:
   - If it does, narrow the search space to that half.
   - If it does not, search the other half.
4. Repeat the process using binary search until the target is found or the pointers cross.

---

## ⏱️ Complexity Analysis

* **Time Complexity:** $O(\log n)$ — The search space is cut in half with every iteration.
* **Space Complexity:** $O(1)$ — Uses a constant amount of extra space for pointers.

---

## 🚀 Getting Started & Running Locally

### Prerequisites
* Java Development Kit (JDK) installed on your machine.

### Compilation and Execution
1. Save the code into a file named `Solution.java`.
2. Open your terminal or command prompt and compile the file:
   ```bash
   javac Solution.java
