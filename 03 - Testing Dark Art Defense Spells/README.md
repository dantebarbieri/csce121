# Basic Linear Algebra
## Overview
This assignment focuses on the vector operations that one may wish to perform in Linear Algebra and other functions that may be beneficial when studying vectors.

Vectors are essentially a list of values, and in a mathematical sense, we treat each value as the extent to which the vector exists in the dimension represented by the index (position) of the coordinate in the vector. Traditionally we tend to focus on R<sup>3</sup> in our math courses, but vectors can be *n* dimensional or R<sup>*n*</sup>.

In the next assignment, you will implement these operations to perform some of these operations. The same code would also be useful to scientists working in research laboratories addressing challenges such as weather forecasting, producing animated movies, designing more efficient batteries, or scheduling airline pilots to minimize flight departure delays. Before that, however, in this assignment, you will write unit tests for a subset of the basic spells.

The operations you must test are:
1. `amax` &mdash; Index of the first element with maximum absolute value
2. `asum` &mdash; Sum of the absolute values of a vector's elements.
3. `axpy` &mdash; Add a scalar multiple of a vector, "`a` times `x` plus `y`" (`y = a*x + y`)
4. `copy` &mdash; Copy vector `x` into vector `y`.
5. `dot` &mdash; Compute the dot product of two vectors.
6. `norm2` &mdash; Compute the Euclidean norm (i.e. magnitude, or length) of a vector.
7. `scale` &mdash; Multiply a vector by a scalar (`x = a*x`).
8. `swap` &mdash; Swap vectors `x` and `y`.

## Objectives
1. Write test cases for unit tests.
2. Read unit-testing results.
3. Persevere through a problem that seems complicated.

## Starter Code
Review the starter code. Doing so will help you with your test cases (i.e. what are the parameters of spells).
- `linalg.h`
- `linalg_tests.txt`

## Requirements
When developing your solution to this problem, ensure that your solution conforms to the following requirements and assumptions:
- [ ] Name the text file containing the test cases `linalg_tests.txt`.
  - [ ] This is the only file you will work on for this assignment. It is a text file, not a file containing code.
  - [ ] A valid version of this file is included in the starter code.
- [ ] Refer to `linalg.h` in the starter code for function declarations and descriptions.
  - [ ] The starter code can be found here.
  - [ ] You won't need to edit them right now, but you can look at them.
- [ ] Do not implement the functions yet, just write the test cases.
- [ ] Refer to `linalg_tests.txt` for test case formatting.
  - [ ] The general form of the test cases is:  
`function ; inputs ; outputs`  
Inputs are comma-separated in the same order as function parameters.
    - [ ] Vectors are specified as space-separated lists.
    - [ ] An example of a valid test case the `amax` function is shown here:
      - [ ] Go to `linalg.h` and find the prototype/declaration for `amax` and you will see that `amax` has two input parameters (`x`, a vector and `len`, the number of elements in `x`) and returns the index of the maximum value in `x`. You will find equivalent information in `linalg_tests.txt`.  
      First you list the function name followed by a semicolon  
      `amax ;`  
      Next you list the parameters. The first is a vector, so put the numbers in with spaces in between and add a comma to separate the first parameter from the second  
      `amax ; 8 6 7 5 3 0 9 ,`  
      Then add the second parameter which is the length or the number of elements in the vector.  
      `amax ; 8 6 7 5 3 0 9 , 7`  
      Add a semicolon to separate the inputs from the expected output.  
      `amax ; 8 6 7 5 3 0 9 , 7 ;`  
      Finally, put the expected return value at the end.   
      `amax ; 8 6 7 5 3 0 9 , 7 ; 6`  
    - [ ] In some instances, there is no return value. Rather, one or more of the input vectors are modified. In those cases, list the vectors indicated in `linalg_tests.txt` from the starter code. For example, a `swap` test case might look like this.  
    `// swap ; x , y , len ; expected x , expected y`  
    `swap ; 3.5 -1.2 4.8 , -5.9 2.2 -3.3 , 3 ; -5.9 2.2 -3.3 , 3.5 -1.2 4.8`

At a minimum you must create test cases that cover the following scenarios
- For every function:
  - 0-dimensional vectors (vectors with 0 elements)
  - Negative values in the input vectors
  - Numbers with fractional parts
- For `amax`: the maximum value is negative, 0, positive; the vector has 1 element.
- For `asum`: the sum is 0, positive
- For `axpy` and `scale`: the scalar is negative, 0, positive > 1
- For `copy` and `swap`: vectors are distinct
- For `dot`: the result is negative, 0, positive
- For `norm2`: the result is 0, positive