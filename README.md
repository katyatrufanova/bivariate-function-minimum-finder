# Bivariate Function Minimum Finder

## Project Overview

This project implements and compares two numerical optimization methods - the Steepest Descent method and Newton's method - to find the minimum of a specific bivariate function. 

![min](https://github.com/user-attachments/assets/16ffa8e3-6c33-47f9-8c94-defdfae11eb9)

## Key Features

- Implementation of Steepest Descent and Newton's method for optimization
- Comparison of both methods in terms of convergence speed and accuracy
- Visualization of the objective function and optimization results
- Calculation and analysis of convergence order for both methods

## The Objective Function

The project focuses on finding the minimum of the following bivariate function:

f(x) = (1/2) * 0.001(x₁-1)² + (x₁²-x₂)²

The known minimum of this function is at x* = (1, 1)ᵀ.

## Methodology

1. Both optimization methods are implemented from scratch.
2. The same starting point and stopping criterion (||∇f(xₖ)||₂ < 10⁻⁴) are used for both methods.
3. The performance of both methods is compared by:
   - Number of iterations required
   - Final approximation of the minimum
   - Function value at the approximated minimum
4. Convergence order is calculated and analyzed for both methods.
5. Results are visualized using 3D plots to provide intuitive understanding.

## Results

The project demonstrates the effectiveness of both methods in finding the minimum of the given function. Newton's method generally converges faster and provides a more accurate approximation compared to the Steepest Descent method.

Detailed results and analysis can be found in the Jupyter notebook and the accompanying report.

## Usage

1. Clone this repository
2. Install the required packages
3. Open and run the Jupyter notebook `bivariate_function_minimum.ipynb`

## Future Work

Potential areas for expansion of this project include:
- Implementation of additional optimization methods for comparison
- Application to more complex multivariate functions
- Analysis of performance with different starting points and stopping criteria
