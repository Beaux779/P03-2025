# P03 – Improved Insertion Sort Performance Analysis

## Overview
This project evaluates the performance of two sorting algorithms:
1. Regular Insertion Sort  
2. Binary Insertion Sort (Improved Version)

The program measures and compares their execution times over multiple runs and array sizes to analyze the efficiency difference between the two.

---

## How It Works
- The program generates random integer arrays of sizes 1,000 through 10,000 (in increments of 1,000).
- Each size is tested 20 times to obtain consistent timing data.
- Both algorithms sort the same randomly generated data for fair comparison.
- Results are written to separate `.dat` files for analysis or visualization.

| Output File | Description |
|--------------|-------------|
| `unsorted.dat` | Randomly generated input arrays |
| `sorted1.dat` | Output of regular insertion sort |
| `sorted2.dat` | Output of binary insertion sort |
| `time1.dat` | Execution times (seconds) for insertion sort |
| `time2.dat` | Execution times (seconds) for binary insertion sort |

---

## Algorithms

### 1. MyInsertionSort
Uses a linear search to find the correct insertion position.  
- **Best Case:** O(n)  
- **Average/Worst Case:** O(n²)

### 2. MyImprovedSort
Uses a binary search to find the insertion position.  
This reduces the number of comparisons but not the number of shifts.  
- **Best Case:** O(n)  
- **Average/Worst Case:** O(n²)

---

## Analyzing Results
1. Combine `time1.dat` and `time2.dat` into a CSV or spreadsheet.
2. Assign array sizes (1,000–10,000) to each group of 20 runs.
3. Plot the data:
   - X-axis: Array Size  
   - Y-axis: Time (seconds)
4. Both algorithms exhibit quadratic growth, but the binary version should run slightly faster for larger input sizes.

---

## Compilation and Usage
```bash
g++ p03.cpp -o P03
./P03 unsorted.dat sorted1.dat sorted2.dat time1.dat time2.dat
