# Square Root Bisection Method

## Overview
This program was created as part of the FreeCodeCamp curriculum to practice Python programming and problem-solving.

This repository contains a Python program to approximate the square root of a non-negative number using the bisection method. It is a simple, iterative approach that narrows down the range of possible values for the square root until it converges within a specified tolerance.

## Features
- Approximates the square root of any non-negative number.
- Allows customization of:
  - Tolerance (default: `1e-7`)
  - Maximum iterations (default: `100`)
- Handles edge cases like square roots of `0` and `1`.
- Detects if the algorithm fails to converge within the maximum iterations.


### Example
Input: `N = 16`  
Output: `The square root of 16 is approximately 4.0`

## How It Works
1. **Initial Range**: The algorithm starts with a range from `0` to `max(1, square_target)`.
2. **Midpoint Calculation**: Repeatedly calculates the midpoint of the range.
3. **Narrowing the Range**: Compares the square of the midpoint with the target value:
   - If the difference is less than the tolerance, the midpoint is the result.
   - Otherwise, the range is updated by setting the new bounds.
4. **Convergence**: Stops when the result converges within the tolerance or the maximum iterations are reached.

## Code Explanation
### `square_root_bisection(square_target, tolerance=1e-7, max_iterations=100)`
- Computes the square root of a non-negative number using the bisection method.
- Raises a `ValueError` if the input is negative.
- Prints the result if the root is found or an error message if it fails to converge.

### Example Usage
```python
N = 25
square_root_bisection(N, tolerance=1e-8)
