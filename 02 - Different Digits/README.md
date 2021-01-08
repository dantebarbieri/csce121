# Different Digits
## Overview
In a distant country, a queen is very superstitious and does not like numbers with odd numbers of repeated digits like 777, 43434, or 2221. Thus, she declares any number with repeated digits to be invalid. You have been appointed by Her Majesty to write a program that, given two integers ***a*** and ***b***, determines how many valid numbers exist between ***a*** and ***b***, inclusive.

Examples:
- For `a=3` and `b=12`, the answer is 9.
- For `a=12` and `b=34`, the answer is 21.

## Objectives
1. Another example of the use of standard input and output;
2. Familiarity with selections, iterations, and simple functions;
3. Importance of designing interesting test cases.

## Requirements
When developing your solution to this problem, ensure that your program conforms to the following requirements and assumptions:
- [ ] Name the source file containing the `main` function `different_digits.cpp`.
- [ ] Implementation is written such that it is readable by other programmers. Use descriptive variable identifiers and comments where appropriate (comments should explain things that are not obvious from the code).
- [ ] You cannot use `string` variables in this assignment.
- [ ] The input/output format should be as follows. The input is given by two integers `a` and `b` such that 0 < `a` &le; `b` &le; 10,000.  
IO format (user input in ***bold italics***; everything else is output):  
> Enter numbers 0 < `a` &le; `b` &le; 10,000: ***12*** ***34***  
There are 21 valid numbers between 12 and 34

> Enter numbers 0 < `a` &le; `b` &le; 10,000: ***-7*** ***10***  
Invalid input

> Enter numbers 0 < `a` &le; `b` &le; 10,000: ***12*** ***100230***  
Invalid input

> Enter numbers 0 < `a` &le; `b` &le; 10,000: ***121*** ***62***  
Invalid input

> Enter numbers 0 < `a` &le; `b` &le; 10,000: ***1*** ***5***  
There are 5 valid numbers between 1 and 5

> Enter numbers 0 < `a` &le; `b` &le; 10,000: ***121*** ***122***  
There are 0 valid numbers between 121 and 122

- [ ] Your code should check if the input is valid: the numbers are positive integers, the second one is greater than or equal to the first, and so on. If the input does not meet the requirements, the output should be "`Invalid input`".
- [ ] Your program must define and use the following functions:
```cpp
/*
This function returns the boolean value `true`
if and only if inputs `a` and `b` satisfy the
constraint that 0 < `a` <= `b` <= 10000.
*/
bool is_valid_range(int a, int b);

/*
This function returns how many times `digit`
occurs in `number`, where 0 <= `digit` <= 9.
*/
int count_digit_occurrences(int number, int digit);

/*
This function returns the boolean value `true`
if and only if `number` contains an odd number
of repeated digits.
*/
bool has_odd_repeated_digits(int number);

/*
This function returns how many numbers in the
range [`a`, `b`] (i.e. `a` <= `number` <= `b`)
are valid according to the queen's
superstition, i.e. how many numbers do not
contain an odd number of repeated digits,
where 0 < `a` <= `b` <= 10000
(i.e. [`a`, `b`] is a valid range).
*/
bool count_valid_numbers(int a, int b);
```
These functions must be submitted in a separate file `functions.cpp` along with the corresponding header file `functions.h` which contains the declarations of these functions. The header file must be included at the beginning of `different_digits.cpp` and `functions.cpp`. For example, `different_digits.cpp` should begin with:
```cpp
#include <iostream>
#include "functions.h"
```
A convenient way to compile multiple source files (in this case the two files: `functions.cpp` and `different_digits.cpp`) is to move the files to a directory (for example, `src`) and run `g++` in this directory with file globbing. In a terminal:
```sh
$ mkdir src
$ mv different_digits.cpp src
$ mv functions.cpp src
$ mv functions.h src
$ cd src
$ g++ -std=c++17 -Wall -Wextra -pedantic -Weffc++ -g *.cpp
```
The `*` symbol is a wildcard that globs all files ending in `.cpp` (in this case) together. This means that it writes `functions.cpp different_digits.cpp` for us. We do not compile `.h` files, so this is an ideal way to compile when all of the code is in a directory unto itself.

`-std=c++17` means that we are using the 2017 version of the c++ programming language.

`-Wall` means that we want to see all Warnings (this doesn't quite show everything).

`-Wextra` means that we want to see extra Warnings.

`-pedantic` means that we want to see pedantic warnings and errors. (*pe-dan-tic: Characterized by a narrow, often ostentatious concern for academic knowledge and formal rules.*)

`-Weffc++` uses warnings defined in the Effective C++ programming textbook.

`-g` includes debugging symbols meaning that the compiling takes a little longer but that it will be easier to find and fix difficult errors that throw signals (e.g. Segmentation Fault, `throw`, `raise`, `abort`, etc.).