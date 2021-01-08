# Change Maker
## Overview
You have been tasked to write a program that makes change with the minimum number of coins and banknotes possible for a given amount &mdash; a 'Change Maker' if you will. For example, &pound;3.50 consists of 1 &pound;2 coin, 1 &pound;1 coin, and 1 50p coin: 0 notes and 3 coins total.

## Objectives
1. Exposure to reading and writing data via standard input and standard output, respectively.
2. Familiarity with: the declaration of variables, reading and writing to the objects bound to them, and interacting with those names objects throughout our program code
3. Experience working with arithmetic types and the operations that can be performed on them.

## Requirements
When developing your solution to this problem, ensure that your program meets the following requirements:
- [ ] Name the source file containing the `main` function `changemaker.cpp`
- [ ] Source code is written such that it is readable by a novice programmer. Use descriptive variable identifiers and comments where appropriate (e.g. for non-trivial program code).
- [ ] Assume an unlimited number of each type of note or coin is available: &pound;50, &pound;20, &pound;10, &pound;5, &pound;2, &pound;1, 50p, 20p, 10p, 5p, 2p, and 1p.
- [ ] The input is read from standard input (i.e. `cin`). **It's never recommended to use floating-point numbers when dealing with monetary values**; therefore you can choose to read in the number of pounds and pence separately
    - [ ] You can first prompt for the number of pounds
    - [ ] Then you can prompt for the number of pence  
    **OR**
    - [ ] You can read in the value as a string and split it into the various parts
- [ ] If change is being made for a value less than &pound;1 (e.g. &pound;0.24), assume that the number of pounds is 0. If change is being made for a value with no pence (e.g. &pound;12.00), assume that the number of pence is 0.
- [ ] Make change with the minimum number of coins for the given amount. You can accomplish this using modulo (`%`) and division (`/`).
- [ ] The output is printed to standard output (i.e. `cout`). Print the number of notes and coins of each denomination, ignoring denominations with 0, and the total number of notes and coins.

- [ ] Format output like so (input is in **bold**):
> Number of pounds (&pound;): **13**  
> Number of pence (p): **34**  
&pound;10 &ndash; 1  
&pound;2 &ndash; 1  
&pound;1 &ndash; 1  
20p &ndash; 1  
10p &ndash; 1  
2p &ndash; 2  
Total Notes and Coins: 7
