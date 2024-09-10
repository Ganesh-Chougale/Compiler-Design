> # 5. Intermediate Code Generation
Intermediate code generation is a pivotal step in compiler design where the source code is translated into a more machine-independent representation. intermediate representation (IR).

1. **Three-Address Code (TAC)**: A sequence of instructions, each with at most three operands.  
2. **Control Flow Graphs (CFGs)**: Graphical representations of the control flow of a program.  
3. **Abstract Syntax Trees (ASTs)**: Hierarchical representations of the program's syntax.



**Three-Address Code (TAC)**:  
Example:
```C++
int a = 10, b = 5, x = 7 , y = 3;
int result = (x + y) * (a - b);
```

```Bash
t1 = (x + y) = (7 + 3)  = 10    // Intermediate result of the addition
t2 = (a - b) = (10 - 5) = 5     // Intermediate result of the subtraction
t3 = t1 * t3 = 10 * 5   = 50    // Final result of the multiplication
```
so untimately  
```Bash
result = 50;
```

**Control Flow Graphs (CFGs)**:
Example:
```C++
if (x > y) {
    z = x;
} else {
    z = y;
}
```
```sql
      +----+
      |    |
      | 1  |  // Entry Block
      |    |
      +----+
        |
        V
      +----+
      |    |
      | 2  |  // Condition Check: x > y
      |    |
      +----+
        |True
        V
      +----+
      |    |
      | 3  |  // Block for z = x
      |    |
      +----+
        | 
        V
      +----+
      |    |
      | 4  |  // End Block
      |    |
      +----+
        |False
        V
      +----+
      |    |
      | 5  |  // Block for z = y
      |    |
      +----+
        |
        V
      +----+
      |    |
      | 4  |  // End Block (common exit)
      |    |
      +----+
```

**Abstract Syntax Trees (ASTs)**:
Example:  
```C++
result = (x + y) * (a - b);
```
```Bash
          (*)
         /   \
       (+)   (-)
      / \    / \
     x   y  a   b
```