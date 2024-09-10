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
c   : variable
=   : assign to operator
a   : variable
+   : addition operator
b   : variable
+   : addition operator 
10  : constant value
;   : semicolon (end of statement)
```

## Tokens

```bash
Keywords:       int, for, class
Identifiers:	variable names
Operators:      +, =, ==, %
Literals:       "textLiteral", 10
Delimiters:     ; . () {} [] ,
```
Explaination
```bash
# Keywords: a special words reserved by language which have specific behaviour & logic
Keywords:       int, for, class, if
```
```bash
# Identifiers: names given to variable, class, function or other enteties
Identifiers:       isLogged, isAdult, setCount
```
```bash
# Operators: operational operators like
 Arithmetic:        +, -, *, /, %
 Relational:        ==, !=, >, <, >=, =<
 Logical:           &&, ||, !
 Assignment:        =, +=, -=, *=, /=, %=
 Ment:              ++, --
 Bitwise:           &, |, ^, ~, <<, >>
 Ternary:           ? :
 Member Access:     ., ->          
```