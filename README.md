# C++ Vector Off-by-One Error

This repository demonstrates a common off-by-one error when iterating over a `std::vector` in C++.  The error arises from incorrectly using `<=` in the loop condition, attempting to access an element beyond the valid index range of the vector.

## Bug Description

The `bug.cpp` file contains a simple program that iterates through a vector.  The loop condition `i <= vec.size()` is incorrect.  Vectors are zero-indexed; therefore, the last valid index is `vec.size() - 1`. Accessing `vec[vec.size()]` results in undefined behavior, potentially leading to a crash or unexpected results. 

## Solution

The `bugSolution.cpp` file corrects the error by changing the loop condition to `i < vec.size()`. This ensures that the loop iterates through all valid elements of the vector without exceeding the bounds.