## Compiler Design
![0101](../Images/0101.jpg)

> 1. Removal of Preprocessor Directives
Example:
```C++
#include <stdio.h>
```
OR 
```C++
// Preprocessor prefixes
#include
#define
// conditional compilation  prefixes
#ifdef
#ifndef
```

> 2. Tokenization

Example:
```C++
int c = a + b + 10;
```

here is how tokenazation happens
```bash
int c = a + b + 10;
int|c|=|a|+|b|+|10|;
int : type operator
c : variable
= : assign to operator
a : variable
+ : addition operator
b : variable
+ : addition operator 
10: constant value
; : semicolon (end of statement)
```