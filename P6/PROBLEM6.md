# Problem 6. Checkerboard Pattern Printing in C `(20 points)`

## Problem Description
Implement a set of functions in C to print various patterns using loops and conditional statements. The program should allow users to print lines, general patterns, checkerboard patterns, and a variant with column-based alternation.

## Required Functions

### 1. `void printLine(char c, int n)`
Prints a line of character `c`, repeated `n` times.

#### Implementation Steps:
1. Initialize a loop variable `i` to 1.
2. Use a `while` loop that runs from `1` to `n`.
3. Inside the loop, print character `c`.
4. If `i` is not the last iteration (`i < n`), print a space after `c`.
5. Increment `i` in each iteration.
6. After the loop ends, move to a new line.




**Example:**
```c
printLine('#', 5);
```
**Output:**
```
# # # # #
```

### 2. `void printLinePattern(char c1, char c2, int n)`
Prints a single line of length `n`, alternating between `c1` and `c2`.

**Example:**
```c
printLinePattern('#', '.', 5);
```
**Output:**
```
# . # . #
```

### 3. `void printCheckerboard(char c1, char c2, int size)`
Prints a checkerboard pattern of size `size × size`, alternating between `c1` and `c2`.

**Example:**
```c
printCheckerboard('#', '.', 5);
```
**Output:**
```
# . # . #
. # . # .
# . # . #
. # . # .
# . # . #
```
*Hint: `printCheckerboard` can reuse `printLinePattern` for efficient implementation.*

### 4. `void printColumnSwapCheckerboard(char c1, char c2, int size)`
Prints a pattern where characters alternate **every column** instead of every row.

**Example:**
```c
printColumnSwapCheckerboard('#', '.', 5);
```
**Output:**
```
# # # # #
. . . . .
# # # # #
. . . . .
# # # # #
```
*Hint: `printColumnSwapCheckerboard` can use `printLine` for efficient implementation.*

## Main Function
In the `main` function:
1. Scan for two characters (`c1`, `c2`) and an integer (`n`). When you scan a character add a space in front of a conversion specifier `" %c"`.
2. Call the functions in the following order:
   - `printLine(c1, n);`
   - `printLinePattern(c1, c2, n);`
   - `printCheckerboard(c1, c2, n);`
   - `printColumnSwapCheckerboard(c1, c2, n);`

**Output:**
```
Enter the first character: #
Enter the second character: *
Enter an integer: 5
# # # # #
# * # * #
# * # * #
* # * # *
# * # * #
* # * # *
# * # * #
# # # # #
* * * * *
# # # # #
* * * * *
# # # # #
```
