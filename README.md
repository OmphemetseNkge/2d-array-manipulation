# 2d-array-manipulation
🗃️ Two Dimensional Array Manipulation in Java | Tutoring notes by Omphemetse Nkge

---

## 📌 Overview

A **two-dimensional (2D) array** consists of rows and columns — essentially a **table** or **matrix**. You access elements using two indices: `matrix[row][col]`.

```
matrix[0][0]  matrix[0][1]  matrix[0][2]
matrix[1][0]  matrix[1][1]  matrix[1][2]
matrix[2][0]  matrix[2][1]  matrix[2][2]
```

---

## 🧠 Table of Contents

- [Declaring a 2D Array](#-declaring-a-2d-array)
- [Initialization](#-initialization)
- [Printing](#-printing)
- [Input](#-input)
- [Sum by Row](#-sum-by-row)
- [Sum by Column](#-sum-by-column)
- [Largest Element in Each Row](#-largest-element-in-each-row)
- [Largest Element in Each Column](#-largest-element-in-each-column)
- [Quick Reference Cheatsheet](#-quick-reference-cheatsheet)
- [Exercises](#-exercises)

---

## 📝 Declaring a 2D Array

```java
// Syntax
dataType[][] arrayName = new dataType[rows][cols];

// Example: 3 rows, 4 columns
int[][] matrix = new int[3][4];

// Access with:
// matrix.length        → number of rows
// matrix[row].length   → number of columns in that row
```

---

## ✏️ Initialization

Set every element in the matrix to a fixed value (e.g., `10`):

```java
for (int row = 0; row < matrix.length; row++) {
    for (int col = 0; col < matrix[row].length; col++) {
        matrix[row][col] = 10;
    }
}
```

> 💡 Java automatically initializes numeric arrays to `0` — use this loop when you need a custom starting value.

---

## 🖨️ Printing

Display the entire matrix row by row:

```java
for (int row = 0; row < matrix.length; row++) {
    for (int col = 0; col < matrix[row].length; col++) {
        System.out.printf("%d\t", matrix[row][col]);
    }
    System.out.println();  // New line after each row
}
```

**Example Output:**
```
10  10  10  10
10  10  10  10
10  10  10  10
```

---

## 📥 Input

Read values from the user into the matrix:

```java
Scanner console = new Scanner(System.in);

for (int row = 0; row < matrix.length; row++) {
    for (int col = 0; col < matrix[row].length; col++) {
        matrix[row][col] = console.nextInt();
    }
}
```

---

## ➕ Sum by Row

Calculate and print the total of each row:

```java
for (int row = 0; row < matrix.length; row++) {
    int sum = 0;
    for (int col = 0; col < matrix[row].length; col++) {
        sum = sum + matrix[row][col];
    }
    System.out.println("Sum of row " + (row + 1) + " = " + sum);
}
```

**Example:**
```
Row 1: [3, 5, 7, 2] → Sum of row 1 = 17
Row 2: [4, 6, 1, 9] → Sum of row 2 = 20
```

---

## ➕ Sum by Column

Calculate and print the total of each column:

```java
for (int col = 0; col < matrix[0].length; col++) {
    int sum = 0;
    for (int row = 0; row < matrix.length; row++) {
        sum = sum + matrix[row][col];
    }
    System.out.println("Sum of column " + (col + 1) + " = " + sum);
}
```

**Example:**
```
Col 1: matrix[0][0], matrix[1][0], matrix[2][0] → Sum of column 1 = ...
```

---

## 🏆 Largest Element in Each Row

Find and display the largest value in each row:

```java
for (int row = 0; row < matrix.length; row++) {
    int largest = matrix[row][0];  // Assume first element is largest

    for (int col = 1; col < matrix[row].length; col++) {
        if (largest < matrix[row][col]) {
            largest = matrix[row][col];
        }
    }

    System.out.println("Largest element of row " + (row + 1) + " = " + largest);
}
```

> ⚠️ Notice: the inner loop starts at `col = 1` because we've already stored `matrix[row][0]` as the initial largest.

---

## 🏆 Largest Element in Each Column

Find and display the largest value in each column:

```java
for (int col = 0; col < matrix[0].length; col++) {
    int largest = matrix[0][col];  // Assume first row element is largest

    for (int row = 1; row < matrix.length; row++) {
        if (largest < matrix[row][col]) {
            largest = matrix[row][col];
        }
    }

    System.out.println("Largest element of column " + (col + 1) + " = " + largest);
}
```

---

## 📋 Quick Reference Cheatsheet

| Operation | Outer Loop | Inner Loop |
|-----------|-----------|------------|
| Initialize | `row` | `col` |
| Print | `row` | `col` |
| Input | `row` | `col` |
| Sum by Row | `row` | `col` |
| Sum by Column | `col` | `row` |
| Largest per Row | `row` | `col` (start at 1) |
| Largest per Column | `col` | `row` (start at 1) |

> 💡 **Key Rule:** `matrix.length` gives the number of **rows**. `matrix[row].length` gives the number of **columns** in that row.

---

## 🧩 Exercises

### Exercise 1 – Matrix Operations
Create a `4x4` integer matrix and write code to:
- ✅ Initialize all values using keyboard input
- ✅ Print the matrix in table format
- ✅ Calculate the sum of each row
- ✅ Calculate the sum of each column
- ✅ Find the largest element in each row
- ✅ Find the largest element in each column

### Exercise 2 – Diagonal Sum
Write a program that finds the **sum of the main diagonal** (top-left to bottom-right) of a square matrix.

```
Hint: Main diagonal elements are where row == col
matrix[0][0], matrix[1][1], matrix[2][2], ...
```

---

## 📬 Contact & Tutoring

| | |
|--|--|
| **Tutor** | Omphemetse Nkge |
| **Module** | Programming Fundamentals |
| **Topic** | Two Dimensional Array Manipulation |

> *"Once you understand 2D arrays, you unlock the ability to model the real world — from grids and tables to images and game boards."*
> — Omphemetse Nkge
