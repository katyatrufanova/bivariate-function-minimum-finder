# Minimum of Bivariate Function

## Introduction

The steepest descent method and the Newton method are both iterative methods for finding the minimum of a function. Starting from an initial estimate x₀, these methods generate a sequence of improved estimates (called "iterates"). The strategy used to move from one iterate to the next distinguishes one algorithm from the other. Each new iterate xₖ₊₁ has a lower function value compared to xₖ.

## Line Search Strategy

Both methods use the line search strategy, where each iterate is computed as:

xₖ₊₁ = xₖ + α pₖ

The goal is to iteratively move in the direction pₖ by a step length αₖ to find a new iterate with a lower function value.

### Steepest Descent Method

In the case of the steepest descent method:

pₖ = -∇fₖ

and

xₖ₊₁ = xₖ - α∇f(xₖ)

Since the gradient indicates the direction of steepest ascent, the negative gradient points at the direction in which to move to decrease the value of the function the fastest (thus this is called the steepest descent method).

### Newton Method

In the Newton method, the direction pₖ is:

pₖ = -Hf(xₖ)⁻¹∇fₖ

and so

xₖ₊₁ = xₖ - αHf(xₖ)⁻¹∇fₖ

## Implementation

The two methods were implemented as follows:

1. The objective function and its minimum were defined.
2. The objective function gradient and Hessian were specified.
3. The steepest descent method was implemented with the stopping criterion ||∇f(xₖ)||₂ < 10⁻⁴.
4. The convergence order p of the steepest descent method was calculated using the provided formula.
5. The Newton method was implemented similarly, with the key difference in how the iterates are computed.
6. Approximations with each method were computed using the same starting point x₀.
7. The function value at the real solution x* was computed to facilitate comparison.

## Results Visualization

The obtained results were plotted in an interactive graph to visualize the function, its minimum, and the minimum approximations obtained with the two different methods.

![min](https://github.com/user-attachments/assets/01afb64b-2ad9-41c6-ba7f-05745fc7d4f9)

## Analysis

Given the presented results, it can be observed that the approximation obtained with the Newton method is quite close to the actual solution compared to the result of the steepest descent method, achieving this result with a smaller number of iterations.

## Convergence Order

The convergence order of both methods was computed using the provided formula. However, it yielded incorrect results. The resulting graphs are shown below:

![steepest_descent](https://github.com/user-attachments/assets/c98dcce9-9845-4423-8342-caa195941d23)

![newton](https://github.com/user-attachments/assets/986ef5a9-e644-4426-890b-a26dbbf7e10b)

## Conclusion

This study demonstrates the effectiveness of both the steepest descent and Newton methods in finding the minimum of a bivariate function. The Newton method showed superior performance in terms of accuracy and convergence speed. Further investigation is needed to understand the discrepancies in the calculated convergence orders.
