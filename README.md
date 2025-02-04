# F# Mutable Variable Swap Bug

This repository demonstrates a common mistake when working with mutable variables in F#.  The issue arises from a misunderstanding of how mutable variables are passed to and handled within functions.

## The Bug

The `bug.fs` file contains code that attempts to swap two mutable variables using a function. However, the function does not correctly swap the original variables. This is because the function receives copies of the variables and only modifies these copies, leaving the original variables unchanged.

## The Solution

The `bugSolution.fs` file presents the corrected code that effectively swaps the two mutable variables.  It correctly uses the `&` operator to pass the variables by reference so that the function can modify their values directly.

## How to reproduce

1. Clone this repository.
2. Open `bug.fs` in an F# environment (like the F# Interactive).
3. Compile and run the code to see that the variables are not correctly swapped.
4. Open `bugSolution.fs` and repeat step 3 to observe the correct swapping of the mutable variables.
